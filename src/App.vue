<template>
  <v-row>
    <v-col class="gsk_logo" md="12" cols="12">
      <img
        alt="gsk logo"
        class="d-flex justify-center align-center"
        src="./assets/gsk_logo.png"
    /></v-col>
    <v-col class="mt-4" md="12" cols="12"
      ><Form msg="Welcome to Your Vue.js App"
    /></v-col>
  </v-row>
</template>

<script>
import Form from "./components/form.vue";

export default {
  name: "App",
  components: {
    Form,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.gsk_logo {
  background: #efefef;
  min-height: 150px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
