<template>
  <nav>
    <router-link to="/">Home</router-link>
  </nav>
  <router-view/>
</template>

<script lang="ts">
import './assets/base.css';

export default {
  name: "App",
};

</script>
<style>
#app {
  text-align: center;
  height: 100vh;
  display: flex;
  flex-direction: column;
}

nav {
  padding: 30px;
  height: 60px;
}

nav a {
  font-weight: bold;
}
</style>
