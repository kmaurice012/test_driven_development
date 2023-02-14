<template>
  <div>
    <input type="text" data-test="messageText" v-model="inputText" />
    <button data-test="sendButton" @click="send">Send</button>
 
  
</div>
</template>

<script>
export default {
  name: "NewMessageForm",
  data() {
    return {
      inputText: "",
    };
  },
  method: {
    send() {
      this.$emit("send", this.inputText);
      this.inputText = "";
    },
  },
};
</script>
