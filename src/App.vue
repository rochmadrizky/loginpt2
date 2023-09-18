<script setup>
import BtnLogin from "./components/BtnLogin.vue";
import InputPassword from "./components/InputPassword.vue";
import InputUsername from "./components/InputUsername.vue";
</script>

<template>
  <div class="min-h-screen flex items-center justify-center bg-gray-100">
    <div class="bg-white p-8 rounded-lg shadow-md w-96">
      <h1 class="text-2xl font-semibold mb-4">Login to SimoLabs?</h1>

      <InputUsername
        type="text"
        label="Username"
        id="username"
        placeholder="Your username"
      />

      <InputPassword
        type="password"
        label="Password"
        id="password"
        placeholder="Your password"
      />

      <BtnLogin>Login</BtnLogin>

      <div class="text-center py-2">
        <a href="#" class="text-sm text-blue-500">Forgot your password?</a>
      </div>
      <div class="text-center">
        <p class="text-gray-600 text-sm">
          Don't have an account? <a href="#" class="text-blue-500">Sign up</a>
        </p>
      </div>
    </div>
  </div>
</template>
