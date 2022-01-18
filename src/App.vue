<template>
  <div id="app">
    <nav-bar v-if="!$route.fullPath.includes('login')"></nav-bar>
    <router-view></router-view>
  </div>
</template>

<script>
import NavBarVue from "./components/NavBar.vue";

export default {
  name: "App",
  components: {
    NavBarVue,
  },
};
</script>

<style scoped>
#app {
  margin: 0 auto;
  width: 70vw;
}
</style>
