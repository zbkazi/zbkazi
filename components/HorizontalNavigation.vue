<script setup lang="ts">
import { useRoute } from 'vue-router';
const route = useRoute();

const links = [{
  label: 'Home',
 icon: 'i-heroicons-home',
  to: '/'
}, {
  label: 'About',
  icon: 'i-heroicons:at-symbol',
  to: '/about'
}, {
  label: 'Horizontal Navigation',
  icon: 'i-heroicons-chart-bar',
  to: '/me'
}, {
  label: 'Command Palette',
  icon: 'i-heroicons-command-line',
  to: '/skills'
}];
</script>

<template>
  <UHorizontalNavigation :links="links" class="border-b border-gray-200 dark:border-gray-800" />
</template>
