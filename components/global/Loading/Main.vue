<template>
  <div :class="{ fixed }" class="loading-mack flex-box">
    <img src="../../../assets/image/svg/loading.svg" />
  </div>
</template>

<script>
export default {
  componentName: "Loading",
  data() {
    return {
      fixed: false
    }
  },
  methods: {
    close() {
      this.$destroy(true)
      this.$el.parentNode.removeChild(this.$el)
    }
  }
}
</script>

<style scoped lang="less" type="text/less">
@import "../../../assets/style/color";
@import "../../../assets/style/config";
@import "../../../assets/style/mixin";

.loading-mack {
  position: absolute;
  z-index: @mask-index;
  background-color: fade(white, 90);
  margin: 0;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  transition: opacity 0.3s;
}

.fixed {
  position: fixed;
}
</style>
