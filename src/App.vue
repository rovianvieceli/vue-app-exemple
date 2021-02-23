<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <router-link class="nav-link" :to="'/'">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" :to="'/contact'">Contact</router-link>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import Posts from "./components/Posts";
import Contact from "./components/Contact";

export default {
  name: "App",
  components: {
    Posts,
    Contact
  }
};
</script>

<style>
@import "../node_modules/bootstrap/dist/css/bootstrap.min.css";
</style>
