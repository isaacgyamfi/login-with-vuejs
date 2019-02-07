<template>
  <div class="home">
    <navbar/>
    <login/>
  </div>
</template>

<script>
// @ is an alias to /src
import login from '@/components/login.vue'
import navbar from '@/components/navbar.vue'

export default {
  name: 'home',
  components: {
    login, navbar
  }
}
</script>
<style scoped>

.home {
}
</style>
