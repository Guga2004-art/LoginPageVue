<template>
  <EstudoVue></EstudoVue>
</template>

<script>
import EstudoVue from "./components/EstudoVue.vue";

export default {
  name: "App",
  components: {
    EstudoVue,
  },
};
</script>

<style>
body {
  background-color: rbg(26, 26, 26);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
