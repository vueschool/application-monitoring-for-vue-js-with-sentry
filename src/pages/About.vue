<script setup>
const user = {};
const makeToast = () => {
  sliceBread();
};
</script>
<template>
  <div>
    <h1 class="text-4xl">About</h1>
    <button @click="user.email.send()">Send Email</button>
    <button @click="makeToast">Make Toast</button>
  </div>
</template>
