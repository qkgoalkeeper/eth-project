<template>
  <div class="leftMenu">
    <el-menu :default-active="onRoutes" theme="dark" class="el-menu-vertical-demo" @open="handleOpen"
             @close="handleClose" router>
<!--      <el-menu-item index="/home/"><i class="el-icon-view"></i>关于我</el-menu-item>-->
      <el-menu-item index="/order_home/basetable"><i class="el-icon-tickets"></i>全部订单</el-menu-item>
      <el-menu-item index="/order_home/sendorder"><i class="el-icon-plus"></i>发起订单</el-menu-item>
      <el-menu-item index="/order_home/myorder"><i class="el-icon-date"></i>我发布的订单</el-menu-item>
      <el-menu-item index="/order_home/myreceiveorder"><i class="el-icon-dessert"></i>我接收的订单</el-menu-item>
      <el-menu-item index="/order_home/myself"><i class="el-icon-water-cup"></i>我的信息</el-menu-item>
<!--      <el-menu-item index="/home/mainActive"><i class="el-icon-menu"></i>主页</el-menu-item>-->
<!--      <el-menu-item index="/home/markdown"><i class="el-icon-edit"></i>markdown</el-menu-item>-->
    </el-menu>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  },
  computed: {
    onRoutes() {
      return this.$route.path.replace('/', '');
    }
  }
}
</script>
<style lang="scss">
.leftMenu {
  display: block;
  position: fixed;
  bottom: 0;
  top: 60px;
  width: 190px;
  left: 0;
  z-index: 999;
  ul {
    height: 100%;
    border-radius: 0;
  }
}
</style>
