<template lang="html">
  <div class="">
    {{ name }}
    <nuxt-link to="mine">Go to mine</nuxt-link>
  </div>
</template>

<script>
export default {
  asyncData() {
    return new Promise(resolve => {
      setTimeout(function() {
        resolve({ name: 'recipe' })
      }, 1000)
    })
  }
}
</script>

<style scoped>
</style>
