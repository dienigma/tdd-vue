<template>
  <div>
    <input type="text" data-test="messageText" v-model="inputText" />
    <button type="button" data-test="sendButton" @click="send">Send</button>
  </div>
</template>

<script setup>
import { ref, defineEmits } from 'vue';

const emit = defineEmits(['send']);

const inputText = ref('');

const send = () => {
  emit('send', inputText.value);
  inputText.value = '';
};
</script>
