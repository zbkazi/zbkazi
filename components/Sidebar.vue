<template>
  <div>
    <aside class="bg-gray-800 w-64 h-screen">
      <div class="p-4">
        <h2 class="text-white text-lg font-semibold">Sidebar</h2>
        <nav class="mt-4">
          <ul>
            <li v-for="link in links" :key="link.to" class="mb-2">
              <router-link :to="link.to" class="flex items-center text-white">
                <i :class="link.icon + ' mr-2'"></i>
                <span>{{ link.label }}</span>
              </router-link>
            </li>
          </ul>
        </nav>
      </div>
    </aside>
  </div>
</template>

<script setup lang="ts">
import { useRoute } from 'vue-router';

const route = useRoute();

const links = [
  {
    label: 'Home',
    icon: 'i-heroicons-home',
    to: '/'
  },
  {
    label: 'About',
    icon: 'i-heroicons:at-symbol',
    to: '/about'
  },
  {
    label: 'Horizontal Navigation',
    icon: 'i-heroicons-chart-bar',
    to: '/me'
  },
  {
    label: 'Command Palette',
    icon: 'i-heroicons-command-line',
    to: '/skills'
  }
];
</script>

<style scoped>
/* Add any additional styling here */
</style>
