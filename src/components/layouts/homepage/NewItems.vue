<script setup>
import CardItem from "@/components/CardItem.vue";
import { ref } from "vue";
const items = ref([
  {
    title: "Mobile UI Kit",
    subtitle: "Mobile UI Kit",
    img: "img/items-1.jpg",
  },
  {
    title: "Online Doctor Consultation",
    subtitle: "Mobile UI Kit",
    img: "img/items-2.jpg",
  },
  {
    title: "Banking Crypto",
    subtitle: "Mobile UI Kit",
    img: "img/items-3.jpg",
  },
]);
</script>

<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">New Items</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <CardItem
        v-for="(item, index) in items"
        :title="item.title"
        :subtitle="item.subtitle"
        :img="item.img"
        :key="index"
        column="3"
      />
    </div>
  </div>
</template>
