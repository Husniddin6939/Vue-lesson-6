<template>
  <div>
    <h1>Life cycle methods!</h1>
    <h1>Counter:{{ count }}</h1>
    <h1>{{ num }}</h1>
    <button @click="count++">Increment</button>
    <button @click="IncrementNumber">IncrementNumber</button>
    <button @click="toggleComponent">Toggle Component</button>

  </div>
  <HelloWorld v-if="toggle"/>
</template>

<script setup>
import {onMounted, onBeforeMount, ref, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted} from 'vue';
import HelloWorld from "./components/HelloWorld.vue";

let num=1;
const count=ref(1);
const toggle=ref(true)
const IncrementNumber=()=>{
  num++;
}

const toggleComponent =()=>{
  toggle.value=!toggle.value;
}

onMounted(()=>{
  console.log("onMounted");
});

onBeforeMount(() => {
  console.log('onBeforeMount');
  
});

onBeforeUpdate(() => {
  console.log('onBeforeUpdate');
  
});

onUpdated(() => {
  console.log('onUpdate');
  
});

onBeforeUnmount(()=>{
  console.log("onBeforeUnMounted");
});

onUnmounted(()=>{
  console.log("onUnMounted");
});


</script>

<style lang="scss" scoped>

</style>