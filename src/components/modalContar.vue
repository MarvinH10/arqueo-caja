<script setup lang="ts">
import { ref, defineEmits } from 'vue';

interface Denominacion {
    valor: number;
    cantidad: number;
}

const emit = defineEmits(['confirmar', 'cancelar']);

const denominaciones = ref<Denominacion[]>([
    { valor: 200, cantidad: 0 },
    { valor: 100, cantidad: 0 },
    { valor: 50, cantidad: 0 },
    { valor: 20, cantidad: 0 },
    { valor: 10, cantidad: 0 },
]);

const total = ref(0);

const incrementar = (index: number) => {
    denominaciones.value[index].cantidad++;
    calcularTotal();
};

const decrementar = (index: number) => {
    if (denominaciones.value[index].cantidad > 0) {
        denominaciones.value[index].cantidad--;
        calcularTotal();
    }
};

const calcularTotal = () => {
    total.value = denominaciones.value.reduce((sum, den) => {
        return sum + (den.valor * den.cantidad);
    }, 0);
};

const resetear = () => {
    denominaciones.value.forEach(den => den.cantidad = 0);
    total.value = 0;
    emit('cancelar');
};

const confirmar = () => {
    emit('confirmar', total.value);
};
</script>

<template>
    <div class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
        <div class="bg-[#181818] p-6 rounded-lg shadow-xl w-full max-w-md">
            <h2 class="text-white text-xl font-bold mb-4">MONEDAS/BILLETES</h2>

            <div class="space-y-3">
                <div v-for="(den, index) in denominaciones" :key="index"
                    class="flex items-center justify-between bg-[#1E1E1E] p-2 rounded">
                    <button @click="decrementar(index)"
                        class="w-8 h-8 flex items-center justify-center text-white hover:bg-gray-700 rounded">
                        <i class="fas fa-minus"></i>
                    </button>

                    <div class="flex items-center">
                        <span class="text-white">S/. {{ den.valor }}</span>
                        <span class="text-white mx-4">{{ den.cantidad }}</span>
                    </div>

                    <button @click="incrementar(index)"
                        class="w-8 h-8 flex items-center justify-center text-white hover:bg-gray-700 rounded">
                        <i class="fas fa-plus"></i>
                    </button>
                </div>
            </div>

            <div class="mt-4 border-t border-gray-700 pt-4">
                <div class="text-white text-right mb-4">
                    TOTAL: S/. {{ total.toFixed(2) }}
                </div>

                <div class="flex justify-between gap-4">
                    <button @click="confirmar"
                        class="flex-1 bg-green-600 text-white py-2 px-4 rounded hover:bg-green-700 transition-colors">
                        CONFIRMAR
                    </button>
                    <button @click="resetear"
                        class="flex-1 bg-red-600 text-white py-2 px-4 rounded hover:bg-red-700 transition-colors">
                        DESCARTAR
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>