<template>
  <div class="relative flex mt-8 md:mt-0 md:pl-8">
    <i
      class="flex items-center justify-center w-8 h-8 text-gray-700 md:absolute md:top-1/2 md:left-[-26px] md:w-12 md:h-12 md:border md:border-gray-300 md:bg-white md:rounded-lg"
    >
      <slot name="icon"></slot>
    </i>
    <div class="flex-1 ml-4">
      <h3 class="text-lg font-medium text-gray-900 mb-2">
        <slot name="heading"></slot>
      </h3>
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
/* Garis vertikal seperti timeline di mode desktop */
@media (min-width: 1024px) {
  .relative::before,
  .relative::after {
    content: '';
    position: absolute;
    left: 0;
    width: 1px;
    background-color: #d1d5db; /* Tailwind gray-300 */
  }

  .relative::before {
    bottom: 50%;
    height: calc(50% - 25px);
  }

  .relative::after {
    top: 50%;
    height: calc(50% - 25px);
  }

  .relative:first-of-type::before,
  .relative:last-of-type::after {
    display: none;
  }
}
</style>
