<template>
  <div class="mb-4">
    <label for="username" class="block text-gray-700 pb-2 font-semibold">{{
      props.label
    }}</label>
    <input
      :type="props.type"
      :id="props.id"
      class="w-full p-2 border border-gray-300 rounded focus:outline-none focus:ring focus:border-blue-500"
      :placeholder="props.placeholder"
    />
  </div>
</template>

<script setup>
const props = defineProps({
  type: String,
  placeholder: String,
  label: String,
  id: String,
});
</script>
