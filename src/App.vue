<script setup>
import { RouterView } from "vue-router";
import Menu from "./components/Menu.vue";
</script>

<template>
  <header>
    <div class="wrapper">
      <Menu />
    </div>
  </header>

  <RouterView />
</template>

<style>
.wrapper {
  display: inline-block;
  vertical-align: top;
  text-align: center;
  justify-content: center;
  align-items: center;
  margin-right: -150px;
}
</style>
