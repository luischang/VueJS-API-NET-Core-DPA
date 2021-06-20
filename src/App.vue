<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" width="15%" />
    <!-- <HelloWorld msg="Hello Vue in CodeSandbox!" />

    <Alumno nombre="Luis Chang" /> -->
    <Listado />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Alumno from "./components/Alumno.vue";
import Listado from "./components/Listado.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Alumno,
    Listado,
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
</style>
