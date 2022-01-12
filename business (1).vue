<template>
  <div class="grid-1">
    <h1 class="text-center font-bold">
      الأعمال 
    </h1>
    <router-link v-for="item in array" :key="item.id" :to='`/business/${item.path}`'
      class="bg h-32"
      :style="`background-image: url(${item.image})`"
    >
      <div class="w-full h-full bg-gray-800 text-white rounded-xl bg-opacity-60 center font-bold">
        {{ item.title }}
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      array: [
        {
          title: "المتجر",
          image: "https://bit.ly/3Dh4clH",
          path: 'store'
        },
        {
          title: "العمل",
          image: "https://bit.ly/3ohthZj",
          path: 'employee'
        },
        {
          title: "الإعلانات",
          image: "https://bit.ly/3qIaFSi",
          path: 'ads'
        },
      ],
    };
  },
};
</script>
