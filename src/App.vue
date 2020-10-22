<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <transition
      name="view"
      appear
      enter-active-class="animate__animated animate__zoomInRight delay"
      leave-active-class="animate__animated animate__zoomOutLeft"
    >
      <router-view />
    </transition>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      bounce: false,
      roll: false,
      animated: false,
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.delay {
  animation-delay: 1s;
}
</style>
