<script lang="ts">
export default {
  name: "Person",
  data() {
    return {
      name: "John Doe",
      age: 25,
      sum: 1,
    };
  },
  methods: {
    add() {
      this.sum++;
    },
  },
  beforeCreate() {
    console.log("beforeCreate() invoked");
  },
  created() {
    console.log("created() invoked");
  },
  beforeMount() {
    console.log("beforeMount() invoked");
  },
  mounted() {
    console.log("mounted() invoked");
  },
  beforeUpdate() {
    console.log("beforeUpdate() invoked");
  },
  updated() {
    console.log("updated() invoked");
  },
  beforeDestroy() {
    console.log("beforeDestroy() invoked");
  },
  destroyed() {
    console.log("destroyed() invoked");
  },
};
</script>

<template>
  <div class="person">
    <h2>当前求和为:{{ sum }}</h2>
    <button @click="add">点我sum+1</button>
  </div>
</template>
<style scoped>
.person {
  background-color: skyblue;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px;
}
</style>
