<template>
  <div>
    My name is -> 
    <span @click="toggleName">{{ spanText }}</span> 
    <h1>{{ name }}</h1>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
const name = ref('Name is...');
const toggleName = () => {
  name.value = name.value === 'Name is...' ? 'Usama Hassan' : 'Name is...';
};
const spanText = computed(() => (name.value === 'Name is...' ? 'show' : 'hide'));
</script>

<style>
h1 {
  color: #f60000;
}
span {
  color: #249901;
  cursor: pointer;
}
</style>
