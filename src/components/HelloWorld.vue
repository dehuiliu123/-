<template>
  <div>{{ num }}</div>
  <div>{{ s }}</div>
  <div>{{ arr }}</div>
  <button @click="sub">减1</button>

  <button @click="add(1)">加1</button>

  啦啦啦啦啦啦
  <input
    type="text"
    :value="title"
    @input="$emit('update:title', $event.target.value)"
  />
</template>

<script>
import { onMounted, ref, toRefs, watch, h } from "vue";
export default {
  emits: {
    sub() {
      return false;
    },
    "update:title"() {},
  },
  props: ["msg", "title"],
  data() {
    return {
      num: 2,
    };
  },
  methods: {
    add(a) {
      this.num += this.s;
      this.arr.push(1);
      this.count += 1;
    },
    sub() {
      this.$emit("sub", 1);
      console.log("attr", this.$attrs);
      console.log("chi", this.$listeners);
    },
  },
  mounted() {
    console.log(2);
  },
  setup(props) {
    let arr = ref([1, 2, 3]);
    let count = ref(0);
    let { msg } = toRefs(props);
    onMounted(() => {});
    watch(count, (o, n) => {});
    return { s: 2, arr, count };
  },
};
</script>

<style></style>
