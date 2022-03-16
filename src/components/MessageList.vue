<template>
  <ul>
    <li v-for="message in props.messages" :key="message">
      {{ message }}
    </li>
  </ul>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps(['messages']);
</script>
