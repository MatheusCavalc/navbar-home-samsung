<script setup>
import { ref } from 'vue';

const openLojaOnline = ref(false)
const listLojaOnline = ['Comprar Agora', 'Descobrir Ofertas', '#YouMake', 'Telefonia', 'TV e AV', 'Informática', 'Eletrodomésticos', 'Geladeiras BESPOKE', 'Combos', 'Live Shop', 'Gaming HUB', 'Eco Troca', 'Loja Física']
const listProgramadeOfertas = ['Estudantes', 'Empresas', 'Parcerias']
const listPorque = ['Vale Mais - Troca Smart', 'Instalação Grátis', 'Troca Smart', 'Cartão Samsung Itaú']

const openTelefonia = ref(false)
const listTelefonia = ['Descobrir', 'Smartphones', 'Tablets', 'Galaxy Book', 'Smartwatches', 'Galaxy Buds', 'Acessorios', 'One UI', 'Aplicativos & Servicos', 'Presentei com Galaxy', 'Why Galaxy', 'Combos']

const openTVAV = ref(false)
const listRecomendado = ['Quero ajuda para escolher', 'Combos', 'Por que Neo QLED', 'Por que Samsung OLED', 'Por que The Frame', 'Descobrir TVs Lifestyle', 'Melhor TV Samsung para jogos', 'Por que Smart TV Samsung', 'Guia de compra de TV', 'Gaming HUB', 'Eco Troca', 'MICRO LED Novo']
const listTv = ['Descobrir TVs', 'Neo QLED', 'QLED', 'OLED Novo', 'The Frame', 'The Serif', 'The Sero', 'Crystal UHD', 'Acessórios', 'Ver Todos']
const listTvs = ['85 polegadas', '75 polegadas', '70 polegadas', '65 polegadas', '60 polegadas', '55 polegadas', '50 polegadas', '43 polegadas', '32 polegadas', 'Ver Todos']
const listTvReso = ['TVs 8K', 'TVs 4K', 'Full HD/HD']
const listProjetores = ['The Premiere', 'The Freestyle', 'Ver Todos']
const listAudio = ['Descobrir Áudio', 'Soundbar Série Q', 'Soundbar Série S', 'Sound Tower', 'Ver Todos']

const openEletrodomesticos = ref(false)
const listRecomendadoEle = ['Descobrir Eletrodomesticos', 'WindFree', 'Connected Living', 'Ar-condicionado ideal para voce', 'Cuide-se Bem. Fique Seguro', 'SmartThings Home', 'Eco Troca', 'Combos']
const listGeladeiras = ['Ver Todos', 'Geladeiras BESPOKE', 'Geladeira French Door', 'Geladeira Side by Side', 'Geladeira Duplex Inverse', 'Geladeira Duplex', 'Acessorios', 'Descobrir Geladeiras']
const listMaquinas = ['Ver Todos', 'Maquina de Lavar', 'Lava e Seca', 'Secadora', 'Descobrir Maquinas de Lavar e Secar']
const listAspiradores = ['Ver Todos', 'Aspiradores Verticais Sem Fio', 'Aspirador Robo', 'Descobrir Aspiradores']
const listLavaLoucas = ['Ver Todos', 'Descobrir Lava-Loucas']
const listArC = ['Ver Todos', 'WindFree', 'Digital Inverter Ultra', 'Multi Split', 'Sistema de Ar Condicionado', 'Ideal para voce']

const openInformatica = ref(false)
const listGalaxy = ['Descobrir Galaxy Book', 'Galaxy Book3 Ultra', 'Galaxy Book3 360', 'Galaxy Book3', 'Galaxy Book2 Pro', 'Galaxy Book2 360', 'Galaxy Book2', 'Galaxy Book S', 'Galaxy Book GO', 'Samsung Book', 'Windows 11', 'Samsung Chromebooks', 'Ver Todos']
const listGalaxyPorTamanho = ['Descobrir Galaxy Book por tamanho', '15"', '13"', '11"', 'Ver Todos']

const openMonitores = ref(false)
const listRecomendadoMonitores = ['Monitor Odyssey Ark', 'Monitor Odyssey', 'Monitores de Alta Resolucao ViewFinity', 'Por que Monitores Smart', 'Combos']
const listMonitores = ['Descobrir Monitores', 'Smart Monitor', 'Odyssey', 'Alta Resolucao', 'Convencional', 'Ver Todos']
const listDisplay = ['Smart Signage', 'LED Signage', 'TVs Comerciais']

</script>

<template>
    <div>
        <div class="hidden w-full md:block md:w-auto">
            <ul
                class="flex flex-col font-medium p-4 md:p-0 mt-4 mr-24 ml-10 whitespace-nowrap border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-1 md:mt-0 md:border-0 md:bg-white">
                <li class="py-4" @mouseover="openLojaOnline = true" @mouseleave="openLojaOnline = false">
                    <button id="dropdownNavbarLink"
                        data-dropdown-toggle="dropdownNavbar"
                        class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
                        :class="{ 'bg-black text-white': openLojaOnline }">Loja
                        Online
                    </button>

                    <!-- Dropdown menu -->
                    <Transition duration="550" name="nested">
                        <div id="dropdownNavbar" v-show="openLojaOnline" @mouseover="openLojaOnline = true"
                            @mouseleave="openLojaOnline = false"
                            class="absolute mt-4 right-340 origin-top-right divide-y divide-gray-100 rounded-b-lg bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none">
                            <div class="flex text-xs justify-between">

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Comprar Agora
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listLojaOnline">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Programa de Ofertas
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listProgramadeOfertas">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Por que comprar no Samsung.com?
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listPorque">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                            </div>
                        </div>
                    </Transition>
                </li>
                <li class="py-4" @mouseover="openTelefonia = true" @mouseleave="openTelefonia = false">
                    <button id="dropdownNavbarLink"
                        data-dropdown-toggle="dropdownNavbar"
                        class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
                        :class="{ 'bg-black text-white': openTelefonia }">Telefonia
                    </button>
                    <!-- Dropdown menu -->
                    <Transition duration="550" name="nested">
                        <div id="dropdownNavbar" v-show="openTelefonia" @mouseover="openTelefonia = true"
                            @mouseleave="openTelefonia = false"
                            class="absolute mt-4 right-340 origin-top-right divide-y divide-gray-100 rounded-b-lg bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none">
                            <div class="flex justify-between text-xs">

                                <div>
                                    <ul class="py-2 text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listTelefonia">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div class="px-10 pb-4">
                                    <p class="text-bold mt-2 py-2">
                                        New and Featured
                                    </p>

                                    <div class="flex justify-between">
                                        <div>
                                            <div class="w-28 h-32 rounded-lg bg-green-100"></div>
                                            <div class="w-28 h-32 mt-3 rounded-lg bg-green-100"></div>
                                            <div class="w-28 h-32 mt-3 rounded-lg bg-green-100"></div>
                                        </div>
                                        <div class="ml-5">
                                            <div class="w-28 h-32 rounded-lg bg-green-100"></div>
                                            <div class="w-28 h-32 mt-3 rounded-lg bg-green-100"></div>
                                            <div class="w-28 h-32 mt-3 rounded-lg bg-green-100"></div>
                                        </div>
                                        <div class="ml-5">
                                            <div class="w-28 h-32 rounded-lg bg-green-100"></div>
                                            <div class="w-28 h-32 mt-3 rounded-lg bg-green-100"></div>
                                            <div class="w-28 h-32 mt-3 rounded-lg bg-green-100"></div>
                                        </div>
                                    </div>
                                </div>

                            </div>
                        </div>
                    </Transition>
                </li>
                <li class="py-4" @mouseover="openTVAV = true" @mouseleave="openTVAV = false">
                    <button id="dropdownNavbarLink"
                        data-dropdown-toggle="dropdownNavbar"
                        class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
                        :class="{ 'bg-black text-white': openTVAV }">TV
                        & AV
                    </button>

                    <!-- Dropdown menu -->
                    <Transition duration="550" name="nested">
                        <div id="dropdownNavbar" v-show="openTVAV" @mouseover="openTVAV = true"
                            @mouseleave="openTVAV = false"
                            class="fixed overflow-x-hidden mt mb-32 mx-10 rounded-b-lg overflow-y-auto inset-0 z-50 shadow-lg ring-1 ring-black ring-opacity-5">
                            <div class="flex text-xs justify-between">

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Recomendados
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listRecomendado">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        TVs
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listTv">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Tvs por tamanho de tela
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listTvs">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Tvs por resolucao
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listTvReso">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Projetores
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listProjetores">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Audio
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listAudio">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                            </div>
                        </div>
                    </Transition>
                </li>
                <li class="py-4" @mouseover="openEletrodomesticos = true" @mouseleave="openEletrodomesticos = false">
                    <button
                        id="dropdownNavbarLink" data-dropdown-toggle="dropdownNavbar"
                        class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
                        :class="{ 'bg-black text-white': openEletrodomesticos }">Eletrodomesticos
                    </button>

                    <!-- Dropdown menu -->
                    <Transition duration="550" name="nested">
                        <div id="dropdownNavbar" v-show="openEletrodomesticos" @mouseover="openEletrodomesticos = true"
                            @mouseleave="openEletrodomesticos = false"
                            class="fixed overflow-x-hidden mt mb-60 mx-10 rounded-b-lg overflow-y-auto inset-0 z-50 shadow-lg ring-1 ring-black ring-opacity-5">
                            <div class="flex text-xs justify-between">

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Recomendado
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listRecomendadoEle">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Geladeiras
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listGeladeiras">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Maquinas de Lavar e Secar
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listMaquinas">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Aspiradores
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listAspiradores">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Lava-loucas
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listLavaLoucas">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Ar-Condicionado
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400" aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listArC">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                            </div>
                        </div>
                    </Transition>
                </li>
                <li class="py-4" @mouseover="openInformatica = true" @mouseleave="openInformatica = false">
                    <button
                        id="dropdownNavbarLink" data-dropdown-toggle="dropdownNavbar"
                        class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
                        :class="{ 'bg-black text-white': openInformatica }">Informatica
                    </button>

                    <!-- Dropdown menu -->
                    <Transition duration="550" name="nested">
                        <div id="dropdownNavbar" v-show="openInformatica" @mouseover="openInformatica = true"
                            @mouseleave="openInformatica = true"
                            class="absolute mt-4 right-340 origin-top-right divide-y divide-gray-100 rounded-b-lg bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none">
                            <div class="flex text-xs justify-between">

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Galaxy Book
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listGalaxy">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Galaxy Book por tamanho
                                    </p>

                                    <ul class="py-2 text-sm text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listGalaxyPorTamanho">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                            </div>
                        </div>
                    </Transition>
                </li>
                <li class="py-4" @mouseover="openMonitores = true" @mouseleave="openMonitores = false">
                    <button id="dropdownNavbarLink"
                        data-dropdown-toggle="dropdownNavbar"
                        class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white"
                        :class="{ 'bg-black text-white': openMonitores }">Monitores
                    </button>

                    <!-- Dropdown menu -->
                    <Transition duration="550" name="nested">
                        <div id="dropdownNavbar" v-show="openMonitores" @mouseover="openMonitores = true"
                            @mouseleave="openMonitores = true"
                            class="absolute mt-4 right-340 origin-top-right divide-y divide-gray-100 rounded-b-lg bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none">
                            <div class="flex justify-between text-xs">

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Recomendado
                                    </p>

                                    <ul class="py-2 text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listRecomendadoMonitores">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Monitores
                                    </p>

                                    <ul class="py-2 text-sm text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listMonitores">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                                <div>
                                    <p class="text-bold px-4 py-2">
                                        Displays
                                    </p>

                                    <ul class="py-2 text-sm text-gray-700 dark:text-gray-400"
                                        aria-labelledby="dropdownLargeButton">
                                        <li v-for="item in listDisplay">
                                            <a href="#"
                                                class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">{{
                                                    item }}</a>
                                        </li>
                                    </ul>
                                </div>

                            </div>
                        </div>
                    </Transition>
                </li>
                <li class="py-4">
                    <a href="#"
                    class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white">Acessorios</a>
                </li>
                <li class="py-4">
                    <a href="#"
                    class="flex items-center justify-between py-1 px-2 rounded-full w-auto hover:bg-black hover:text-white">SmartThings</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.nested-enter-active {
    transition: all 0.3s ease-in-out;
}

.nested-leave-active {
    transition: all 0.08s ease-in-out;
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

.mt {
    margin-top: 62px;
}
</style>