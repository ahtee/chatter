<template>
  <b-navbar id="navbar" toggleable="md" type="dark" variant="dark">
    <b-navbar-brand href="#">Chatter</b-navbar-brand>
    <b-navbar-nav class="ml-auto">
      <b-nav-text v-if="user.name">{{ user.name }} |</b-nav-text>
      <b-nav-item href="#" active>Logout</b-nav-item>
    </b-navbar-nav>
  </b-navbar>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "nav-bar",
  computed: {
    ...mapState(["user"])
  }
};
</script>

<style>
#chat-navbar {
  margin-bottom: 15px;
}
</style>