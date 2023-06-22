<script setup>
import FirstMenu from '@/components/navbar/navbar-menus/FirstMenu.vue'
import SecondMenu from '@/components/navbar/navbar-menus/SecondMenu.vue'
import ThirdMenu from '@/components/navbar/navbar-menus/ThirdMenu.vue'
</script>

<template>
  <nav class="bg-white border-gray-200 dark:bg-gray-900 dark:border-gray-700">
    <div class="w-full flex items-center justify-between px-4 text-sm border">

      <!--LOGO-->
      <div class="py-3">
        <a href="#" class="">
          <span class="self-center logo mb-1 font-semibold whitespace-nowrap dark:text-white">Samsung</span>
        </a>
      </div>

      <!--Primeira Lista-->
      <FirstMenu />

      <!--Segunda Lista-->
      <SecondMenu />

      <!--Terceira Lista-->
      <ThirdMenu />

    </div>
  </nav>
</template>

<style scoped>
.logo {
  font-size: 1.5rem;
}
</style>