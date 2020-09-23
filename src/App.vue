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
import db from "./db";
// import firebase from "firebase";

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
    db.collection("users")
      .doc("GiyYHGayb6PWvOVUcVs3")
      .get()
      .then(snapshot => {
        this.user = snapshot.data().name;
      });
  }
};
</script>
<style lang="scss">
@import "node_modules/bootstrap/scss/bootstrap";
</style>
