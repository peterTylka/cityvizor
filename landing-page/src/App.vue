<template>
  <div id="app"
    class="l-wrapper"
    :class="[{ 'is-home' : isHome }]">
    <!-- Header -->
    <Header 
      :isHome="isHome"
     ></Header>

    <!-- Main -->
    <router-view></router-view>
    
    <!-- Footer -->
    <Footer></Footer>
  </div>
</template>

<script>
import Header from './components/partials/Header.vue'
import Footer from './components/partials/Footer.vue'

export default {
  name: 'app',
  components: {
    Header,
    Footer
  },
  computed: {
    isHome() {
      return this.$route.path === '/';
    }
  },
  data() {
  },
  created() {
  },
  methods: {
  }
}
</script>

<style lang="scss">
@import './assets/styles/main';
</style>
