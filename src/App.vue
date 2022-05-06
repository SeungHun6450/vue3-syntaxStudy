<template>
<!-- v-once -->
  <!-- <h1
    v-once
    @click="add">
    {{ msg }}
  </h1> -->

  <!-- v-html -->
  <!-- <h1 v-html="msg"></h1> -->

  <!-- v-bind  -->
  <!-- <h1 :class="msg"> -->
  <!-- 
  <h1 v-bind:class="msg">
    {{ msg }}
  </h1> -->

  <!-- 동적 전달인자 -->
  <h1 
    :[attr]="'active'"
    @[event]="add">
    {{ msg }}
  </h1>
</template>

<script>
export default {
  data() {
    return {
      // v-once
      // msg: 'Hello world!!'

      // v-html
      // msg: '<div style="color: red;">Hello!!</div>'

      // v-bind
      // msg: 'active'

      // 동적 전달인자
      msg: 'active',
      attr: 'class',
      event: 'click'
    }
  },
  methods: {
    add() {
      this.msg += '!'
    }
  }
}
</script>

<style scoped>
  .active {
    color: royalblue;
    font-size: 100px;
  }
</style>

