<script setup>
import { ref, reactive, onMounted } from "vue";
//you can pass the email with ref, then you should use v-model="email" and email.value
const email = ref("");
const password = ref("");
//for reactive you just type user.email, user.password
const user = reactive({
  email: "",
  password: "",
});
const names = reactive([]);
onMounted(() => {
  console.log("component mounted");
  names.push(
    {
      firstName: "Alex",
      age: 30,
    },
    {
      firstName: "John",
      age: 25,
    },
    {
      firstName: "Maria",
      age: 22,
    }
  );
});

function login() {
  console.log("login working");
  console.log(user.email, user.password);
}
function remove(user) {
  const index = names.findIndex((name) => {
    return name.firstName === user.firstName;
  });

  names.splice(index, 1);
}
</script>

<template>
  <h1>Login View</h1>

  <template v-if="names.length > 0">
    <ul>
      <li v-for="name in names">
        {{ name.firstName }} <button @click="remove(name)">remove</button>
      </li>
    </ul>
  </template>
  <template v-else>No user found.</template>

  <template v-if="user.email.length <= 0">Empty e-mail</template>
  <template v-else>{{ user.email }}</template>

  <form action="" @submit.prevent="login">
    <input type="text" placeholder="Email" v-model="user.email" />
    <input type="text" placeholder="Password" v-model="user.password" />
    <button type="submit">Login</button>
  </form>
</template>
