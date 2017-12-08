<template>

</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      radio: '广州'
    }
  },
  methods: {
    tabs: function (info) {
      this.radio = info
    }
  }
}
</script>
<style scoped>
</style>
