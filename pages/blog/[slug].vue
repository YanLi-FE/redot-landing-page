<script setup lang="ts">
import { useRoute } from "#app";
const route = useRoute();

const { data: post } = await useAsyncData("post", () =>
  queryContent()
    .where({ _path: `/blog/${route.params.slug}` })
    .findOne()
);

defineOgImageComponent("RedotOG", {
  title: post.value?.title,
  description: post.value?.description,
  imageUrl: "",
  backgroundColor: "#000000",
  brandColor: "#FF6E01",
});

useSeoMeta({
  title: post.value?.title,
  ogTitle: post.value?.title,
  description: post.value?.description,
  ogDescription: post.value?.description,
});
</script>

<template>
  <div>
    <ContentDoc />
  </div>
</template>
