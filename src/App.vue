<template>
  <div>
    <new-message-form @send="addMessage"></new-message-form>
    <message-list :messages="messages"></message-list>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import NewMessageForm from './components/NewMessageForm.vue';
import MessageList from './components/MessageList.vue';

const messages = ref([]);
const addMessage = (messageText) => messages.value.unshift(messageText);
</script>
