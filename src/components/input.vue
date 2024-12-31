<script>
import ModalContar from './modalContar.vue'

export default {
    components: {
        ModalContar
    },
    data() {
        return {
            showModal: false,
            inputValue: ''
        }
    },
    methods: {
        clearInput() {
            this.inputValue = '';
            const input = this.$el.querySelector("input");
            input.focus();
        },
        toggleModal() {
            this.showModal = !this.showModal;
        },
        handleConfirm(total) {
            this.inputValue = total.toFixed(2);
            this.showModal = false;
        }
    },
};
</script>

<template>
    <div class="relative">
        <div class="flex items-center gap-1">
            <div class="relative w-full">
                <input v-model="inputValue" type="number"
                    class="w-full p-2 pr-10 focus:outline-none border border-gray-300 rounded appearance-none text-black"
                    placeholder="S/. 0.00" />
                <i class="fas fa-times absolute right-3 top-1/2 transform -translate-y-1/2 text-gray-400 cursor-pointer"
                    @click="clearInput"></i>
            </div>
            <div class="bg-green-600 p-2 rounded mt-[0.49px] cursor-pointer" @click="toggleModal">
                <i class="fas fa-money-bill text-white text-xl mt-1"></i>
            </div>
        </div>

        <ModalContar v-if="showModal" @confirmar="handleConfirm" @cancelar="toggleModal" />
    </div>
</template>

<style scoped>
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
    -webkit-appearance: none;
    margin: 0;
}

input[type="number"] {
    -moz-appearance: textfield;
}
</style>