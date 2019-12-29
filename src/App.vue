<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/> -->
    <MainLayout/>
  </div>
</template>

<script>

import MainLayout from '@/layouts/MainLayout'

export default {
  components: {
    MainLayout
  }
}
</script>