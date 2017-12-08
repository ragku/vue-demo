<template>
<el-radio-group v-model="radio">
  <el-radio-button label="上海">
    <i class="el-icon-setting"></i>
  </el-radio-button>
  <el-radio-button label="北京"></el-radio-button>
  <el-radio-button label="广州"></el-radio-button>
</el-radio-group>
</template>

<script>
export default {
  name: 'Email',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
