<template>
  <div>
    <h1 ref="slaw">This is a home page</h1>
  </div>
</template>

<script setup>
import { ref, onMounted, nextTick } from "vue";
const slaw = ref(null);
onMounted(async () => {
  await nextTick(); // Wait for the next DOM update

  console.log(slaw.value.offsetWidth);
});
</script>
