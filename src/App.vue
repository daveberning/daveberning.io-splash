<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'

  export default Vue.extend({
    mounted() {
      // @ts-ignore
      VANTA.NET({
        el: '#app',
        color: 0x0f6f88,
        backgroundColor: 0x7192f
      })
    }
  })
</script>

<style>
  * {
    box-sizing: border-box;
  }

  #app {
    padding: 2rem;
  }
</style>
