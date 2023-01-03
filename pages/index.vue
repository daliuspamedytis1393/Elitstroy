<template>
  <Tutorial />
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
    try {
      const baba = await $content("blog").fetch();
      console.log("baba", baba);
    } catch (err) {
      console.log(err);
    }
  },
};
</script>
