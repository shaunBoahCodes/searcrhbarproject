<template>
  <div class="flex flex-col items-center h-[100vh]" @click.self="toggleShowCatAlt">
    <Searchbar class="mt-10" @showCatClicked="toggleShowCat"></Searchbar>
    <Category v-if="showCat"></Category>
  </div>
</template>

<script>
import './assets/tailwind.css'
import Searchbar from '@/components/Searchbar'
import Category from '@/components/Category.vue'

export default {
  name: 'App',
  components: {
    Searchbar,
    Category
  },
  data() {
    return {
      showCat: false
    }
  },
  methods: {
    toggleShowCat() {
      this.showCat = !this.showCat
    },
    toggleShowCatAlt() {
      if (this.showCat) this.showCat = !this.showCat
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 15px;
}
</style>
