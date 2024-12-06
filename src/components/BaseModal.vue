<template>
  <div
    class="absolute w-full bg-black bg-opacity-30 h-screen top-0 left-0 flex justify-center px-8"
  >
    <div class="p-4 bg-white mt-500 self-start mt-32 max-w-screen">
      <slot />
      <button class="text-white bg-orange-500 py-2 mt-10 px-6">Close</button>
    </div>
  </div>
</template>

<script setup></script>
