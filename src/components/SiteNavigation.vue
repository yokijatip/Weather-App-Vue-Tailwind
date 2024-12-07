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
          @click="toggleModal"
        ></i>
        <i
          class="fa-solid fa-plus text-xl text-black hover:text-weather-secondary duration-500 cursor-pointer ms-6"
        ></i>
      </div>

      <BaseModal :showModal="showModal" @close-modal="toggleModal">
        <div class="text-black">
          <h1 class="text-2xl mb-1">About:</h1>
          <p class="mb-4">
            The Local Weather allows you to track the current and future weather
            of cities of your choosing.
          </p>
          <h2 class="text-2xl">How it works:</h2>
          <ol class="list-decimal list-inside mb-4">
            <li>Search for a city by entering the name into the search bar.</li>
            <li>
              Select a city within the results, this will take you to the
              current weather for your selection
            </li>
            <li>
              Track the city by clicking on the "+" icon in the top right. This
              will save the city to view at a later time on the Home Page
            </li>
          </ol>
          <h2 class="text-2xl">Removing a City:</h2>
          <p>
            If you no longer wish to track a city, simply select the city within
            the home page. At the bottom of the page, there will be a button to
            remove the city.
          </p>
        </div>
      </BaseModal>
    </nav>
  </header>
</template>

<script setup>
import { RouterLink } from "vue-router";
import BaseModal from "./BaseModal.vue";
import { ref } from "vue";

// Variabel Modal State
const showModal = ref(null);
const toggleModal = () => {
  showModal.value = !showModal.value;
};
</script>
