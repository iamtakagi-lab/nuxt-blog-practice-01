<template>
  <div>
    <div class="markdown-body" v-html="$md.render(post.fields.body)"></div>

    <a :href="'https://twitter.com/intent/tweet?text=' + '&url=https%3A%2F%2Fmctech.life%2Fposts%2F' + post.fields.slug + '&hashtags=mctechjp&via=mctechjp&related=mctechjp'" class="twitter-share-button" data-show-count="true" style="margin-top: 20px">Tweet</a>
  </div>

</template>

<script>
    export default {
        name: "Bodytext",
        props: ['post']
    }
</script>

<style scoped lang="scss">
  @import "../../assets/markdown.css";

  .markdown-body {
    box-sizing: border-box;
    min-width: 200px;
    max-width: 980px;
    padding-top: 20px;
    margin: 0 auto;
  }

</style>
