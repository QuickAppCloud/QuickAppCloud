<template>
    <div class="header">
      <div class="logo">
        <span class="header-btn" >
            <img src="@/assets/images/u302.png" alt="">
            菜单
        </span>
      </div>
      <div class="separate"></div>
      <div class="icell">
          <img src="@/assets/images/logo.png" alt="Logo">
      </div>
      <div class="right">
        <span class="header-btn" >
            <img src="@/assets/images/u265.png" alt="">
            敏捷应用云官网
        </span>
        <span class="header-btn" >
            <img src="@/assets/images/u260.png" alt="">
            社区
        </span>
        <span class="header-btn" >
            <img src="@/assets/images/u255.png" alt="">
            应用市场
        </span>
       <span class="header-btn" >
            <img src="@/assets/images/u250.png" alt="">
            开发管理中心
        </span>
        <span class="header-btn" >
            <img src="@/assets/images/u245.png" alt="">
            请登录
        </span>
      </div>
    </div>
</template>
<script>
import EuiFooter from './Footer'
import NavBar from './NavBar'
export default {
  components: {
    EuiFooter, NavBar
  }
}
</script>
<style lang="less">

  .sidebar-hidden {
    .header {
      .logo {
        background: #096DD9;
        .big {
          display: none;
        }
        .min {
          display: block;
        }
        width: 64px;
      }
    }
    .aside{
      .sidebar-toggle{
        .icon-left{
          transform: rotate(180deg);
        }
      }
    }
    .main {
      .app-body {
        margin-left: 64px;
      }
    }
  }
  .sidebar-close{
    .header {
      .logo {
        width: 0;
        overflow: hidden;
      }
    }
    .aside{
     margin-left: -230px;
    }
    .main {
      .app-body {
        margin-left: 0;
      }
    }
  }
  .sidebar-hidden.sidebar-close{
    .aside{
      margin-left: -64px;
    }
  }

  .main {
    display: flex;
    .el-menu:not(.el-menu--collapse) {
      width: 230px;
    }
    .app {
      width: 100%;
      background-color: #ecf0f5;
    }
    .aside {
      position: fixed;
      margin-top: 50px;
      z-index: 10;
      background-color: #222d32;
      transition: all 0.3s ease-in-out;
      .menu{
        overflow-y: auto;
        height: calc(~'100vh - 100px');
      }
      .sidebar-toggle{
        position: relative;
        width: 100%;
        height: 50px;
        background-color: #367fa9;
        color: #fff;
        cursor: pointer;
        .icon-left{
          position: absolute;
          display: flex;
          align-items: center;
          justify-content: center;
          right: 0;
          width: 64px;
          height: 100%;
          font-size: 20px;
          transition: all 0.3s ease-in-out;
        }
      }
    }
    .app-body {
      margin-left: 230px;
      -webkit-transition: margin-left 0.3s ease-in-out;
      transition: margin-left 0.3s ease-in-out;
    }
    .main-container {
      //margin-top: 50px;
      padding: 6px;
      min-height: calc(~'100vh - 101px');
    }
  }

  .header {
    width: 100%;
    position: fixed;
    display: flex;
    height: 40px;
    background-color: #096DD9;
    z-index: 10;
    left: 0;
    top: 0;
    .logo {
      span{
        width: 64px;
        font-size: 13px;
      }
      width: 55px;
      height: 40px;
      text-align: center;
      line-height: 40px;
      color: #CDE1F6;
      font-style:normal;
      font-size:14px;
      font-family:"Arial Normal","Arial";
      position: absolute;
      left:15px;
      top:0;
      background-color: #096DD9;
      -webkit-transition: width 0.35s;
      transition: all 0.3s ease-in-out;
      &:hover {
        color: #ffffff
      }
    }
    .separate{
          width:1px;
          height:18px;
          background:#ffffff;
          position: absolute;
          left: 94px;
          top: 11px;
      }
    .icell{
        position: relative;
        left: 112px;
        top: 11px;
    }
    .right {
      position: absolute;
      right: 15px;
    }
    .header-btn {
        img{
            position: relative;
            top: 3px;
        }
      overflow: hidden;
      height: 40px;
      display: inline-block;
      text-align: center;
      line-height: 40px;
      cursor: pointer;
      padding: 0 9px;
      color: #CDE1F6;
      font-size:12px;
      font-family:"Arial Normal","Arial";
      &:hover {
        color: #ffffff
      }
    }

  }

  .menu {
    border-right: none;
  }

  .el-menu--vertical {
    min-width: 190px;
  }
  .setting-category{
    padding:10px 0;
    border-bottom: 1px solid #eee;
  }
</style>
