<template>
  <div id="app">
    <div>
      <Navigation />
      <router-view class="container" :user="user" />
    </div>
  </div>
</template>
<script>
import Navigation from "./components/Navigation";
// import db from "./db";
import Firebase from "firebase";

export default {
  name: "app",
  components: {
    Navigation
  },

  data() {
    return {
      user: null
    };
  },

  mounted() {
    Firebase.auth().onAuthStateChanged(user => {
      if (user) {
        this.user = user.email;
      }
    });
  }
};
</script>
<style lang="scss">
@import "node_modules/bootstrap/scss/bootstrap";
</style>
