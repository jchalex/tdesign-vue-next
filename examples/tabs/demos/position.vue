<template>
  <div class="t-demo-tabs">
    <div class="t-demo-tabs__desc">
      <t-radio-group v-model="placement" variant="default-filled">
        <t-radio-button value="top"> top </t-radio-button>
        <t-radio-button value="right"> right </t-radio-button>
        <t-radio-button value="bottom"> bottom </t-radio-button>
        <t-radio-button value="left"> left </t-radio-button>
      </t-radio-group>
    </div>
    <t-tabs :value="value" :placement="placement" @change="handlerChange">
      <t-tab-panel value="first" label="选项卡1">
        <p style="padding: 25px">选项卡1</p>
      </t-tab-panel>
      <t-tab-panel value="second" label="选项卡2">
        <p style="padding: 25px">选项卡2</p>
      </t-tab-panel>
      <t-tab-panel value="third" label="选项卡3">
        <p style="padding: 25px">选项卡3</p>
      </t-tab-panel>
    </t-tabs>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const value = ref('first');
const placement = ref('top');

const handlerChange = (newValue) => {
  value.value = newValue;
};
</script>

<style lang="less">
.t-demo-tabs {
  &__desc {
    margin-bottom: 20px;
    color: #333;
    font-size: 14px;

    &:not(:first-of-type) {
      margin-top: 20px;
    }

    p {
      margin-bottom: 20px;
    }
  }

  &__btn {
    margin-right: 20px;
  }
}
</style>
