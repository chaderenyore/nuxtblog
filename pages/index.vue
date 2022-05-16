<template>
	 <div>
    <h1 class="text-5xl font-black text-center">New on the blog</h1>
    <ul class="grid grid-cols-3 gap-8 mt-8">
      <PostPreview v-for="post in articles" :key="post.slug" :post="post"></PostPreview>
    </ul>
  </div>
</template>

<script>
	export default {
		async asyncData({$content, params}) {
			const articles = await $content('blog', params.slug)
											.sortBy('createdAt', 'asc')
											.fetch();
			return { articles }
		}
	}
</script>