<template>
  <div>
    <li v-for="post of posts" :key="post.slug">
      <NuxtLink :to="post.slug">{{ post.title }}</NuxtLink>
    </li>
  </div>
</template>

<script>
export default {
  head() {
    return {
      script: [
        { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" },
      ],
    };
  },
  name: "IndexPage",
  async asyncData({ $content }) {
    // const posts = await $content("blog").fetch();

    return {
      posts,
    };
  },
};
</script>
