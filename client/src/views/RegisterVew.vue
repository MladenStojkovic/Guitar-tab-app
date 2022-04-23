<script setup>
import { ref } from "vue";

import Auth from "@/services/Auth";

const email = ref("");
const password = ref("");

const registerHandler = async () => {
  await Auth.register({
    email: email.value,
    password: password.value,
  });
};
</script>

<template>
  <div>
    <h1>Register</h1>

    <input type="email" name="email" placeholder="email" v-model="email" />
    <input type="password" name="" id="" v-model="password" />
    {{ email }}
    {{ password }}
    <button @click="registerHandler">Register</button>
  </div>
</template>

<style lang="scss" scoped></style>
