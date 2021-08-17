<template>
  <div class="hello">
    {{ count }}
    <button @click="add">+1</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    count: Number,
  },
  methods: {
    add() {
      const value = this.count + 1;
      this.$emit("update:count", value);
    },
  },
};
</script>

