<template>
  <div class="bg">
    <div class="title">{{title}}：</div>
    <div :class="flag?'active':'passive'" @focusin="highlight" @focusout="unhighlight">
      <div class="inputbd"><input type="text"></div>
      <div class="del"></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "myinput",
    props: {
      title: {
        type: String,
        default: "Error"
      }
    },
    data() {
      return {
        flag:false
      }
    },
    methods: {
      highlight:function () {
        this.flag=true
      },
      unhighlight:function () {
        this.flag=false
      }
    }
  }
</script>

<style scoped lang="less">
  @import "myinput";
</style>
