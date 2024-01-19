<script setup>
// import { defineProps } from "vue";
import { useRouter } from "vue-router";

const router = useRouter();

// defineProps(["event"]);
const props = defineProps(["event"]);
const register = () => {
  // if registration API call is successful
  router.push({
    name: "EventDetails",
    // pas obligé, populated by default (id)
    id: props.event.id,
  });
};
</script>
<template>
  <p>Register for the event here</p>
  <button @click="register">Register me !</button>
</template>
