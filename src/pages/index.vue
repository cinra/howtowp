<template>
  <div>
    <h1 class="title">How to build</h1>
    <h2 class="subtitle">the wordpress site</h2>
    <div v-for="post in posts">
      <h3><a :href="post.link">{{ post.title.rendered }}</a></h3>
    </div>
    
    <div class="links">
      <a
        href="https://nuxtjs.org/"
        target="_blank"
        class="btn btn-primary"
      >Documentation</a>
      <a
        href="https://github.com/nuxt/nuxt.js"
        target="_blank"
        class="btn btn-secondary"
      >GitHub</a>
    </div>
  </div>
</template>

<script>

import axios from 'axios'

export default {
  asyncData ({ params }) {
    return axios.get(`http://wp.test/wp/wp-json/wp/v2/posts`)
    .then((res) => {
      return { posts: res.data }
    })
  },
  head() {
    return {
      title: 'TEST'
    }
  }
}

</script>
