<template>
  <nav>
    <div class="nav-buttons">
      <div class="home-select"><RouterLink to="/">Home</RouterLink></div>
      <div class="about-select"><RouterLink to="/about">About</RouterLink></div>
      <div class="login-select"><RouterLink to="/login">Login</RouterLink></div>
    </div>
  </nav>
</template>

<script setup>
import { RouterLink } from "vue-router";
</script>

<style scoped>
nav {
  width: 100%;
  font-size: 30px;
  text-align: center;
  margin-top: 2rem;
}
.home-select {
  padding: 2px;
  text-align: center;
}
.about-select {
  padding: 2px;
  text-align: center;
}
.login-select {
  padding: 2px;
  text-align: center;
}
.nav-buttons {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 5px;
  border: 12px solid hsla(160, 100%, 37%, 1);
  border-radius: 4px;
}
</style>
