<script setup lang="ts">
withDefaults(
  defineProps<{
    title?: string;
    description?: string;
    imageUrl?: string;
    backgroundColor?: string;
    brandColor?: string;
  }>(),
  {
    title: "title",
    description: "description",
    imageUrl: "",
    backgroundColor: "#000000",
    brandColor: "#FF6E01",
  }
);
</script>

<template>
  <div>
    <div>
      <div>
        <h1>
          {{ title }}
        </h1>
        <h2>
          {{ description }}
        </h2>
        <img v-if="imageUrl" alt="" :src="imageUrl" />
        <p>redotengine.org</p>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss"></style>
