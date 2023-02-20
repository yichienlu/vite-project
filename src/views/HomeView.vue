
<template>
  <main>
    HOME
  </main>
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'

export default {
  components: {
    RouterLink, RouterView
  },
  mounted() {
    this.$http.get(import.meta.env.VITE_PATH)
    .then((res) => {
      console.log(res.data)
    })
    .catch((err) => {
      console.log(err)
    })
  }
}
</script>

<style lang="scss">

</style>