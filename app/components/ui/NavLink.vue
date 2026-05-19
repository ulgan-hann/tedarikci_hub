<template>
  <a
    :href="href"
    class="
      px-5 py-3 rounded-full
      text-gray-700 font-medium
      transition-all duration-300

      hover:bg-gray-50
      hover:text-black
      hover:shadow-sm
      hover:-translate-y-0.5
    "
  >
    {{ text }}
  </a>
</template>

<script setup>
defineProps({
  text: String,
  href: String
})
</script>