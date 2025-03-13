<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div class="text-center md:text-left">
    <h1 class="text-4xl font-semibold -mt-2 text-green-500">{{ msg }}</h1>
    <h3 class="text-lg mt-2">
      You’ve successfully created a project with
      <a
        href="https://vite.dev/"
        target="_blank"
        rel="noopener"
        class="text-blue-500 hover:underline"
        >Vite</a
      >
      +
      <a
        href="https://vuejs.org/"
        target="_blank"
        rel="noopener"
        class="text-blue-500 hover:underline"
        >Vue 3</a
      >.
    </h3>
  </div>
</template>
