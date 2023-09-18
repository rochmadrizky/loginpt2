<template>
  <div>
    <div class="mb-4 relative">
      <label for="username" class="block text-gray-700 pb-2 font-semibold">{{
        props.label
      }}</label>
      <input
        :type="showPassword ? 'text' : 'password'"
        :id="props.id"
        class="w-full p-2 border border-gray-300 rounded focus:outline-none focus:ring focus:border-blue-500"
        :placeholder="props.placeholder"
        v-model="password"
      />

      <button
        @click="showPassword = !showPassword"
        class="absolute top-[42px] right-2"
      >
        <img
          v-if="showPassword"
          src="eye-filled.svg"
          alt="Hide Password"
          class="h-6 w-6 text-gray-400 cursor-pointer"
        />
        <img
          v-else
          src="eye-off.svg"
          alt="Show Password"
          class="h-6 w-6 text-gray-400 cursor-pointer"
        />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      password: "",
      showPassword: false,
    };
  },
};
</script>

<script setup>
const props = defineProps({
  type: String,
  placeholder: String,
  label: String,
  id: String,
});
</script>
