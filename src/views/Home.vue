<template>
  <div class="content">
    <img src="@/assets/dave.png" alt="Dave Berning">
    <h1>@daveberning</h1>
    <p>Developer at Oodle.io from Cincinnati, OH.</p>
    <ul>
      <li v-for="media in socialMedia" :key="media.icon">
        <a :href="media.href"><i :class="`fab fa-${media.icon}`"></i></a>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import HelloWorld from '@/components/HelloWorld.vue'

  export default Vue.extend({
    name: 'home',
    components: {
      HelloWorld
    },
    data() {
      return {
        socialMedia: [
          {icon: 'twitter', href: 'https://twitter.com/daveberning'},
          {icon: 'linkedin-in', href: 'https://www.linkedin.com/in/davidberning/'},
          {icon: 'instagram', href: 'https://www.instagram.com/daveberning/'},
          {icon: 'github', href: 'https://www.github.com/daveberning/'}
        ]
      }
    }
  })
</script>

<style lang="scss" scoped>
  .content {
    text-align: center;
  }

  h1 {
    margin-bottom: 1rem;
  }

  p {
    text-align: center;
    line-height: 2.5rem;
  }

  a {
    color: #ffffff;
    font-size: 1.5rem;
  }

  ul li {
    display: inline-block;
    margin: 1rem 1rem 0 0;

    &:last-child {
      margin-right: 0;
    }
  }

  button {
    background: #0f6f88;
    color: #ffffff;
    border: 0;
    padding: .5rem 1.5rem;
    font-size: 1rem;
    border-radius: 100px;
    margin-top: 1rem;
    margin-right: 1rem;

    &:last-child {
      margin-right: 0;
    }
  }
</style>
