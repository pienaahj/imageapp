<template>
 <v-App>
  <!-- SIDEBAR -->
  <SideBar @selectOption="onSelectOption"/>
  <v-main>
    <!-- CARDS -->
    <ImageGallery :isWithColor="isWithColor"/>
  </v-main>
 </v-App>
</template>

<script lang="ts" setup>
  //
  import SideBar from "./components/SideBar.vue";
  import ImageGallery from "./components/ImageGallery.vue";
  import { ref } from "vue";

  const isWithColor = ref(true);

  const onSelectOption = (isColor: boolean) => {
    isWithColor.value = isColor;
  };
</script>
