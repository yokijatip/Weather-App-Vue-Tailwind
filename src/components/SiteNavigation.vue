<template>
  <header class="sticky top-0 bg-weather-primary shadow-lg">
    <nav
      class="container flex flex-col sm:flex-row items-center gap-4 text-black py-6"
    >
      <RouterLink :to="{ name: 'home' }">
        <div class="flex items-center gap-3">
          <i class="fa-solid fa-sun text-2xl"></i>
          <p class="text-2xl text-black">The Local Weather</p>
        </div>
      </RouterLink>

      <div class="flex gap-3 flex-1 justify-end">
        <i
          class="fa-solid fa-circle-info text-xl text-black hover:text-weather-secondary duration-500 cursor-pointer"
        ></i>
        <i
          class="fa-solid fa-plus text-xl text-black hover:text-weather-secondary duration-500 cursor-pointer ms-6"
        ></i>
      </div>

      <BaseModal>
        <h1 class="text-black">Hello From Modal Here</h1>
      </BaseModal>
    </nav>
  </header>
</template>

<script setup>
import { RouterLink } from "vue-router";
import BaseModal from "./BaseModal.vue";
</script>
