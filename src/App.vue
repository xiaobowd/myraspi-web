<template>
  <div id="app">
    <el-container>
      <el-header>
        <nav-header></nav-header>
      </el-header>
      <el-container>
        <el-aside>
          <nav-menu></nav-menu>
        </el-aside>
        <el-main>
          <keep-alive>
            <router-view></router-view>
          </keep-alive>
        </el-main>
      </el-container>
      <el-footer>Footer</el-footer>
    </el-container>
  </div>
</template>

<script>
import NavMenu from '@/components/NavMenu'
import Header from '@/components/Header'

export default {
  name: 'home',
  components: {
    NavMenu: NavMenu,
    NavHeader: Header
  }
}

</script>

<style>
  .el-header {
    text-align: center;
    color: #fff;
    width: 100%;
    background-color: lightskyblue;
    overflow: hidden
  }

  .el-aside {
    margin-top: 5px;
    height: 100%;
  }
  .el-footer {
    text-align: center;
    color: #fff;
    width: 100%;
    background-color: lightskyblue;
    overflow: hidden;
  }

  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
    margin-top: 5px;
    height: 100%;
    margin-left: 5px;
  }

  body > .el-container {
    /*margin-bottom: 40px;*/
  }

  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }

  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>
