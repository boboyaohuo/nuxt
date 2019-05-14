<template lang="html">
  <div class="">
    {{ name }}
    <nuxt-link to="/">Go to /</nuxt-link>
  </div>
</template>

<script>
export default {
  asyncData() {
    return new Promise(resolve => {
      setTimeout(function() {
        resolve({ name: 'mine' })
      }, 1000)
    })
  }
}
</script>

<style scoped>
</style>
