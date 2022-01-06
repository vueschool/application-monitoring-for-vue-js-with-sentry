<script setup>
import * as Sentry from "@sentry/vue";
const user = {};
const post = {
  id: 1,
  title: "Hello world",
  body: "lorem ipsum, blah, blah, blah...",
};

Sentry.setContext("post", {
  id: post.id,
  postTitle: post.title,
});
Sentry.setTag("randomTag", "hello-tag");

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
