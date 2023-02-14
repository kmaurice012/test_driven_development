<template>
  <div>
    <new-message-form />
    <new-message-form @send="addMessage" />
    <message-list :messages="messages" />
  </div>
</template>

<script>
import NewMessageForm from "./components/NewMessageForm";
import MessageList from "./components/MessageList";

export default {
  components: {
    NewMessageForm,
    MessageList,
  },
  name: "App",
  data() {
    return {
      messages: [],
    };
  },
  methods: {
    addMessage(text) {
      this.messages.unshift(text);
    },
  },
};
</script>
