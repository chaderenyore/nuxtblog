<template>
  <li class="transition-all duration-500 ease-in-out">
    <nuxt-link :to="`/blog/${post.slug}`">
      <nuxt-img
        class="rounded-lg"
        :src="post.image"
        preset="preview"
        width="400"
        height="300"
      ></nuxt-img></nuxt-link>
      <ul v-if="post.tags" class="flex space-x-3 mt-2">
        <li class="text-gray-400 font-bold" v-for="tag in post.tags" :key="tag">
          {{ tag }}
        </li>
      </ul>
      <nuxt-link :to="`/blog/${post.slug}`">
        <h2 class="mt-2 text-3xl font-semibold">{{ post.title }}</h2>
      </nuxt-link>
    </a>
  </li>
</template>

<script>
export default {
  props: {
    post: Object,
  }
}
</script>