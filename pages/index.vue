<script setup lang="ts">
import MainPageFeatures from "~/components/MainPage/MainPageFeatures.vue";
defineOgImageComponent("RedotOG", {
  title: "Redot Engine",
  description: "Open‑source Multi-platform 2D and 3D game engine for everyone",
  imageUrl: "",
  backgroundColor: "#000000",
  brandColor: "#FF6E01",
});

useSeoMeta({
  title: "Redot Engine, game engine for everyone",
  ogTitle: "Redot Engine, game engine for everyone",
  description: "Open‑source Multi-platform 2D and 3D game engine",
  ogDescription: "Open‑source Multi-platform 2D and 3D game engine",
});
</script>

<template>
  <MainPageHero />

  <MaxWidthContainer class="main-page-sections">
    <MainPageNews />
    <MainPageFeatures />
    <MainPageGetInvolved />
    <MainPageImprove />
  </MaxWidthContainer>

  <Footer />
</template>

<style scoped>
.main-page-sections {
  display: flex;
  flex-direction: column;
  gap: 80px;
  padding: 80px 0;
}
</style>
