<!-- <script setup lang="ts">
import Input from './components/input.vue'
import Descripcion from './components/descripcion.vue'
</script>

<template>
  <div class="min-h-screen bg-[#181818] text-white flex flex-col gap-8 relative">
    <div class="relative">
      <div class="text-2xl font-bold mt-6 ml-6 mb-6">CONTROL DE CUADRE DE CAJA</div>
      <div class="absolute top-full left-0 w-full border-b border-gray-400"></div>
    </div>

    <div class="bg-white mr-9 ml-9 rounded-md shadow-md mt-20">
      <div class="flex flex-row gap-6 mt-8 ml-5 mr-16 mb-8">
        <div class="bg-white text-[#181818] flex-1 flex flex-col justify-center items-center ml-10">
          <div class="w-full max-w-sm">
            <span class="block font-semibold">Saldo Inicial</span>
            <Input />
            <div class="mt-4">
              <span class="block font-semibold ">Descripción</span>
              <Descripcion />
            </div>
          </div>
        </div>
        <div
          class="bg-[#181818] text-white p-6 rounded-md shadow-md flex flex-row gap-6 w-[1300px] justify-center items-center">
          <div class="flex-2 flex-col">
            <span class="block font-semibold mb-4">MÉTODOS DE PAGO</span>
            <div class="flex flex-col gap-6">
              <div>
                <span class="block font-semibold mb-2">Banco</span>
                <Input />
              </div>
              <div>
                <span class="block font-semibold mb-2">Yape</span>
                <Input />
              </div>
              <div>
                <span class="block font-semibold mb-2">Efectivo</span>
                <Input />
                <div class="mt-4">
                  <span class="block font-semibold mb-2">Descripción</span>
                  <Descripcion />
                </div>
              </div>
            </div>
          </div>
          <div class="flex-1 flex-col ml-9">
            <span class="block font-bold mb-2 text-sm">EFECTIVO CONTADO</span>
            <ul class="mb-2 text-sm">
              <div class="border-l border-gray-500">
                <li class="flex justify-between ml-5 mb-3">
                  <span>Apertura</span>
                  <span>S/. 0.00</span>
                </li>
                <li class="flex justify-between ml-5 mb-3">
                  <span>Pagos en Efectivo</span>
                  <span>S/. 0.00</span>
                </li>
                <li class="flex justify-between ml-5 font-bold mb-3">
                  <span>Total Efectivo</span>
                  <span
                    class="relative before:border-l-[50px] before:block before:absolute before:w-full before:h-[1px] before:bg-gray-500 before:top-0">
                    S/. 0.00
                  </span>
                </li>
              </div>
            </ul>
            <div class="flex justify-between font-bold text-sm mb-3">
              <span>BANCO CONTADO</span>
              <span>S/. 0.00</span>
            </div>
            <div class="flex justify-between font-bold text-sm mb-3">
              <span>YAPE CONTADO</span>
              <span>S/. 0.00</span>
            </div>
            <div class="flex justify-between font-bold text-sm">
              <span class="ml-[700px]">TOTAL</span>
              <span
                class="relative before:border-l-[50px] before:block before:absolute before:w-full before:h-[1px] before:bg-gray-500 before:top-0">
                S/. 0.00
              </span>
            </div>
            <div class="flex justify-end mt-10">
              <button
                class="bg-green-500 hover:bg-green-600 text-white py-2 px-2 rounded shadow flex items-center gap-2">
                <i class="fas fa-file-excel text-white"></i>
                Descargar
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template> -->

<script setup lang="ts">
import Input from './components/input.vue'
import Descripcion from './components/descripcion.vue'
</script>

<template>
  <div class="min-h-screen bg-[#181818] text-white flex flex-col gap-4 md:gap-8 relative">
    <div class="relative">
      <div class="text-xl md:text-2xl font-bold mt-4 md:mt-6 ml-4 md:ml-6 mb-4 md:mb-6">CONTROL DE CUADRE DE CAJA</div>
      <div class="absolute top-full left-0 w-full border-b border-gray-400"></div>
    </div>

    <div class="bg-white mx-4 md:mx-9 rounded-md shadow-md mt-8 md:mt-20">
      <div class="flex flex-col lg:flex-row gap-4 md:gap-6 p-4 md:p-8">
        <div class="bg-white text-[#181818] w-full lg:w-1/4 flex flex-col justify-center items-center">
          <div class="w-full max-w-sm">
            <span class="block font-semibold">Saldo Inicial</span>
            <Input />
            <div class="mt-4">
              <span class="block font-semibold">Descripción</span>
              <Descripcion />
            </div>
          </div>
        </div>

        <div
          class="bg-[#181818] text-white p-4 md:p-6 rounded-md shadow-md flex flex-col lg:flex-row gap-6 xl:w-[1240px] w-full justify-center items-center">
          <div class="flex-1">
            <span class="block font-semibold mb-4">MÉTODOS DE PAGO</span>
            <div class="flex flex-col gap-4 md:gap-6">
              <div>
                <span class="block font-semibold mb-2">Banco</span>
                <Input />
              </div>
              <div>
                <span class="block font-semibold mb-2">Yape</span>
                <Input />
              </div>
              <div>
                <span class="block font-semibold mb-2">Efectivo</span>
                <Input />
                <div class="mt-4">
                  <span class="block font-semibold mb-2">Descripción</span>
                  <Descripcion />
                </div>
              </div>
            </div>
          </div>

          <div class="flex-1 lg:ml-6">
            <span class="block font-bold mb-2 text-sm">EFECTIVO CONTADO</span>
            <ul class="mb-2 text-sm">
              <div class="border-l border-gray-500">
                <li class="flex justify-between ml-5 mb-3">
                  <span><i class="fa-solid fa-plus mr-2"></i> Apertura</span>
                  <span>S/. 0.00</span>
                </li>
                <li class="flex justify-between ml-5 mb-3">
                  <span><i class="fa-solid fa-plus mr-2"></i> Pagos en Efectivo</span>
                  <span>S/. 0.00</span>
                </li>
                <li class="flex justify-between ml-5 font-bold mb-3">
                  <span><i class="fa-solid fa-plus mr-2"></i> Total Efectivo</span>
                  <span
                    class="relative before:border-l-[50px] before:block before:absolute before:w-full before:h-[1px] before:bg-gray-500 before:top-0">
                    S/. 0.00
                  </span>
                </li>
              </div>
            </ul>

            <div class="flex justify-between font-bold text-sm mb-3">
              <span>BANCO CONTADO</span>
              <span>S/. 0.00</span>
            </div>
            <div class="flex justify-between font-bold text-sm mb-3">
              <span>YAPE CONTADO</span>
              <span>S/. 0.00</span>
            </div>
            <div class="flex justify-between font-bold text-sm">
              <span class="ml-auto mr-4">TOTAL</span>
              <span
                class="relative before:border-l-[50px] before:block before:absolute before:w-full before:h-[1px] before:bg-gray-500 before:top-0">
                S/. 0.00
              </span>
            </div>

            <div class="flex justify-end mt-6 md:mt-10">
              <button
                class="bg-green-500 hover:bg-green-600 text-white py-2 px-4 rounded shadow flex items-center gap-2">
                <i class="fas fa-file-excel text-white"></i>
                Descargar
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>