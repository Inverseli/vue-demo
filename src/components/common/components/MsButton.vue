<template>

  <div>
    <el-button v-for="(btn, index) in buttons"
               :key="index"
               @click="click(btn)"
               :size="btn.size"
               :type="btn.type"
               :icon="btn.icon"
    >
      {{btn.tip}}
    </el-button>
  </div>

</template>

<script>
  export default {
    name: "MsButton",
    props: {
      buttons: Array
    },
    methods: {
      click(btn) {
        if (btn.exec instanceof Function) {
          btn.exec();
        }
      }
    }
  }
</script>

<style scoped>

</style>