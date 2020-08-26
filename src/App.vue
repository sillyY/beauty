<template>
  <div class="container">
    <!-- <AnimationButton /> -->
    <checkbox />
  </div>
</template>

<script>
// import AnimationButton from "./components/animation-button.vue";
import checkbox from "./components/checkbox.vue";
export default {
  name: "App",
  components: {
    // AnimationButton,
    checkbox,
  },
};
</script>
<style lang="scss" scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background: #e0e5ec;
}
</style>
