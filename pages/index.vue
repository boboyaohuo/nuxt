<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        {{ name }}
      </h1>
      <nuxt-link to="/recipe">Go to /recipe</nuxt-link>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  asyncData() {
    return new Promise(resolve => {
      setTimeout(function() {
        resolve({ name: 'world' })
      }, 1000)
    })
  },
  components: {
    Logo
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
