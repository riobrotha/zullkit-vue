<script setup>
import { RouterLink } from "vue-router";

const props = defineProps({
  title: String,
  img: String,
  subtitle: String,
  column: String,
});
</script>

<template>
  <div :class="'w-full px-1 my-1 md:w-1/2 lg:my-4 lg:px-4 lg:w-1/' + props.column">
    <div class="overflow-hidden border border-gray-200 rounded-xl">
      <router-link to="#">
        <div class="m-4 overflow-hidden rounded-xl">
          <img
            :alt="props.title"
            class="block w-full h-auto"
            :src="'./src/assets/' + props.img"
          />
        </div>
      </router-link>

      <header class="px-4 mb-4 leading-tight">
        <h1 class="text-lg">
          <router-link
            class="font-semibold text-black no-underline hover:underline"
            to="#"
          >
            {{ props.title }}
          </router-link>
        </h1>
        <span class="block text-sm font-light text-gray-500 no-underline">
          {{ props.subtitle }}
        </span>
      </header>
    </div>
  </div>
</template>
