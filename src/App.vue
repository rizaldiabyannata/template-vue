<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header class="flex flex-col items-center p-6 bg-gray-800 text-white md:flex-row space-x-16">
    <img alt="Vue logo" class="w-16 h-16" src="@/assets/logo.svg" />

    <div class="text-center md:text-left">
      <HelloWorld msg="You did it!" />

      <nav class="mt-4 space-x-4">
        <RouterLink to="/" class="px-4 py-2 rounded hover:bg-gray-700">Home</RouterLink>
        <RouterLink to="/about" class="px-4 py-2 rounded hover:bg-gray-700">About</RouterLink>
      </nav>
    </div>
  </header>

  <main class="px-24 py-16">
    <RouterView />
  </main>
</template>

<style scoped>
.router-link-exact-active {
  color: #38bdf8; /* Warna biru dari Tailwind */
  font-weight: bold;
}
</style>
