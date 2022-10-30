<script setup>
import CardItem from "@/components/CardItem.vue";
import { ref } from "vue";
const categories = ref([
  {
    title: "Mobile UI Kit",
    subtitle: "731 Items",
    img: "img/categories-1.jpg",
  },
  {
    title: "Fonts",
    subtitle: "657 Items",
    img: "img/categories-2.jpg",
  },
  {
    title: "Icon Set",
    subtitle: "83,559 Items",
    img: "img/categories-3.jpg",
  },
  {
    title: "Website UI Kitt",
    subtitle: "4,500 Items",
    img: "img/categories-4.jpg",
  },
]);
</script>
<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Categories</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <CardItem
        v-for="(item, index) in categories"
        :title="item.title"
        :subtitle="item.subtitle"
        :img="item.img"
        :key="index"
        column="4"
      />
    </div>
  </div>
</template>
