<template>
  <div>
    <t-button variant="outline" @click="openSomeMsg"> 点击打开多个消息 </t-button>
    <t-button id="t-demo-msg-close-all" variant="outline" @click="closeAll"> 点击关闭所有消息 </t-button>
  </div>
</template>

<script setup>
import { MessagePlugin } from 'tdesign-vue-next';

const openSomeMsg = () => {
  MessagePlugin.info('这是第一条消息');
  MessagePlugin.warning('这是第二条消息');
  MessagePlugin.error('这是第三条消息');
};
const closeAll = () => {
  MessagePlugin.closeAll();
};
</script>

<style scoped>
.t-button + .t-button {
  margin-left: 16px;
}
</style>
