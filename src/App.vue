<script lang="ts">
import Person from "./components/Person.vue";
export default {
  name: "App",
  components: {
    Person,
  },
  data() {
    return {
      isShow: true,
    };
  },
  methods: {
    toggleShow() {
      this.isShow = !this.isShow;
    },
  },
};
</script>

<template>
  <div>
    <Person v-if="isShow" />
    <button @click="toggleShow">显示/隐藏Person组件</button>
  </div>
</template>
