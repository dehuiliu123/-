<template>
  <HelloWorld :msg="message" @sub="sub" v-model:title="bookTitle" />
  <Setup class="set" ref="aa" :msg="1" :msg2="2" />
  <p ref="p">啦啦啦</p>
  <button @click="awa">假按揭啊</button>
</template>

<script setup>
const p = ref();
const aa = ref();
let bookTitle = ref("袁猪儿");

function awa() {
  console.log(111);
}
onMounted(() => {
  function sub() {
    console.log(1);
  }
});

import { onMounted } from "@vue/runtime-core";
import { ref } from "vue";

// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from "./components/HelloWorld.vue";
import Setup from "./components/setup.vue";
</script>

<style scoped></style>
