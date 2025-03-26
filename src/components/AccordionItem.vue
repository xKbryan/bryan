<template>
  <div class="border border-blue-300 rounded-lg mb-2 overflow-hidden shadow-lg">
    <button 
      class="w-full bg-blue-200 text-blue-900 font-bold py-3 px-4 text-left focus:outline-none flex justify-between items-center transition-all duration-300 hover:bg-blue-300"
      @click="isOpen = !isOpen"
    >
      {{ title }}
      <span>{{ isOpen ? '▲' : '▼' }}</span>
    </button>
    <div v-if="isOpen" class="p-4 bg-white text-gray-700 border-t border-blue-300">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "AccordionItem",
  props: {
    title: String
  },
  data() {
    return {
      isOpen: true
    };
  }
};
</script>

<style scoped>
button {
  transition: background-color 0.3s;
}
button:hover {
  background-color: #bbdefb; /* Azul bebê mais claro ao passar o mouse */
}
</style>
