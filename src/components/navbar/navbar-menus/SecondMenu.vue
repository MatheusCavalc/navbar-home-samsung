<script setup>
import { ref } from 'vue';

const openSuporte = ref(false)
const listProduto = ['Suporte', 'Dicas e Manuais', 'Buscar Suporte', 'Duvidas da Loja']
const listReparo = ['Informacoes de Garantia', 'Localizar Assistencia', 'Agendar Reparo na Assistencia', 'Acompanhar Reparo']
const listFale = ['Chat', 'Telefone', 'Whatsapp', 'E-mail', 'Lingua de Sinais']
</script>

<template>
  <div>
    <div class="hidden w-full md:block md:w-auto" id="navbar-dropdown">
      <ul
        class="flex flex-col font-medium p-4 md:p-0 mt-4 mr-10 whitespace-nowrap border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-1 md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
        <li class="py-4" @mouseover="openSuporte = true" @mouseleave="openSuporte = false">
          <button id="dropdownNavbarLink" data-dropdown-toggle="dropdownNavbar"
            class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
            :class="{ 'bg-black text-white': openSuporte }">Suporte
          </button>

          <!-- Dropdown menu -->
          <Transition duration="550" name="nested">
            <div id="dropdownNavbar" v-show="openSuporte" @mouseover="openSuporte = true"
              @mouseleave="openSuporte = false"
              class="fixed overflow-x-hidden m-100 mr-10 rounded-b-lg overflow-y-auto inset-0 z-50 shadow-lg ring-1 ring-black ring-opacity-5">
              <div class="flex text-xs justify-between">

                <div>
                  <p class="text-bold px-4 py-2">
                    Produto
                  </p>

                  <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                    <li v-for="item in listProduto">
                      <a href="#"
                        class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                          item }}</a>
                    </li>
                  </ul>
                </div>

                <div>
                  <p class="text-bold px-4 py-2">
                    Reparo & Garantia
                  </p>

                  <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                    <li v-for="item in listReparo">
                      <a href="#"
                        class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                          item }}</a>
                    </li>
                  </ul>
                </div>

                <div>
                  <p class="text-bold px-4 py-2">
                    Fale Conosco
                  </p>

                  <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                    <li v-for="item in listFale">
                      <a href="#"
                        class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                          item }}</a>
                    </li>
                  </ul>
                </div>

                <div>
                  <p class="text-bold px-4 py-2">
                    Informacoes Adicionais
                  </p>

                  <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                    <li>
                      <a href="#"
                        class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Noticias &
                        Alertas</a>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </Transition>
        </li>
        <li class="py-4">
          <a href="#"
            class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
            aria-current="page">Empresa</a>
        </li>
        <li class="py-4">
          <a href="#"
            class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
            aria-current="page">Minha Conta</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.nested-enter-active,
.nested-leave-active {
  transition: all 0.3s ease-in-out;
}

/* delay leave of parent element */
.nested-leave-active {
  transition-delay: 0.25s;
}

.nested-enter-from,
.nested-leave-to {
  transform: translateY(30px);
  opacity: 0;
}

/* we can also transition nested elements using nested selectors */
.nested-enter-active .inner,
.nested-leave-active .inner {
  transition: all 0.3s ease-in-out;
}

/* delay enter of nested element */
.nested-enter-active .inner {
  transition-delay: 0.25s;
}

.nested-enter-from .inner,
.nested-leave-to .inner {
  transform: translateX(30px);
  /*
  	Hack around a Chrome 96 bug in handling nested opacity transitions.
    This is not needed in other browsers or Chrome 99+ where the bug
    has been fixed.
  */
  opacity: 0.001;
}

.m-100 {
  margin-left: 520px;
  margin-bottom: 330px;
  margin-top: 62px;
}
</style>