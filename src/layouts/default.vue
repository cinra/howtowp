<template>
  <div>
    <Header />
    <section class="container">
      <nuxt />
    </section>
  </div>
</template>

<script>

import Header from '~/components/Header.vue'
import axios from 'axios'

export default {
  components: {
    Header
  }
}

</script>

<style>

</style>
