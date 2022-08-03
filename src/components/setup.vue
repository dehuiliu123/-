<template>
  <div>{{ b }}</div>
  <div>
    <input type="text" v-focus />
    <button @click="increment">lalala</button>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
const num = ref(0);
const props = defineProps(["msg", "msg2"]);
onMounted(() => {
  console.log(props.msg);
  console.log(props.msg2);
});
defineExpose({
  num: 1,
});
</script>

<style></style>
