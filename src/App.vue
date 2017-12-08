<template>
  <div id="app">
  <!--<el-container>
    <el-header>{{ msg }}</el-header>
    <el-main>
      <el-row :gutter="10">
        <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1"><div class="grid-content bg-purple"></div></el-col>
        <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :xs="4" :sm="6" :md="8" :lg="9" :xl="11"><div class="grid-content bg-purple"></div></el-col>
        <el-col :xs="8" :sm="6" :md="4" :lg="3" :xl="1"><div class="grid-content bg-purple-light"></div></el-col>
      </el-row>
      <router-view/>
    </el-main>
    <el-footer>
      <el-row>
        <el-col :xs="7" :sm="8" :md="6" :lg="6" :xl="1">
          <i class="el-icon-tickets" v-bind:class="{ active: active == 'A' }" v-on:click="tabs('read document!','A')"></i>
        </el-col>
        <el-col :xs="10" :sm="8" :md="12" :lg="12" :xl="11">
          <i class="el-icon-message" v-bind:class="{ active: active == 'B' }" v-on:click="tabs('read email!','B')"></i>
        </el-col>
        <el-col :xs="7" :sm="8" :md="6" :lg="6" :xl="1" >
          <i class="el-icon-setting" v-bind:class="{ active: active == 'C' }" v-on:click="tabs('read setting!', 'C')"></i>
        </el-col>
      </el-row>
    </el-footer>
  </el-container>-->
    <el-tabs :tab-position="bottom">
      <el-tab-pane class="el-icon-tickets" label="用户管理"><router-view/></el-tab-pane>
      <el-tab-pane class="el-icon-message" label="配置管理">配置管理</el-tab-pane>
      <el-tab-pane class="el-icon-setting" label="角色管理">角色管理</el-tab-pane>
    </el-tabs>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      active: 'A'
    }
  },
  methods: {
    tabs: function (info, activeOption) {
      this.msg = info
      this.active = activeOption
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0px 0px 0px 0px;
}
a {
  color: #42b983;
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.el-header {
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  line-height: 60px;
}
.el-tabs {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  text-align: center;
  background-color: #B3C0D1;
  color: #333;
}
.el-footer {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  text-align: center;
  background-color: #B3C0D1;
  color: #333;
}

.el-footer:hover {
  cursor: pointer;
}

.el-footer .el-col:hover,vistor {
  color: #409EFF;
}

.el-footer .el-col i {
   width:100%;
   height:100%;
   line-height: 60px;
}

.active {
  color: #409EFF;
}
</style>
