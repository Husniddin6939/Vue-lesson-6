<template>
  <div>
    <div class="card">
      <h1>Hello World</h1>
    </div>
  </div>
</template>

<script setup>

import {onBeforeUnmount, onUnmounted } from 'vue'

onBeforeUnmount(()=>{
  console.log("onBeforeUnMounted h");
});

onUnmounted(()=>{
  console.log("onUnMounted h");
});


</script>

<style scoped>
.card{
  width: 400px;
  height: 400px;
  display: grid;
  place-content: center;
  margin: 50px;
  background-color: #fee6e6;
}
</style>