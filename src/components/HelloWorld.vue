<template>
  <div class="hello">
    <TopNavigator>
    </TopNavigator>
    <div class="top_container">
    <div class="search_and_cart">
      <div class="wide">
        <div class="logo" style="float: left"><img style="width: 100%" src="https://img10.360buyimg.com/img/jfs/t1/50166/9/22920/11310/63a1993cE3800216e/105f3d456f0905bb.jpg"></div>
        <el-input style="width: 546px;margin-top: 40px;margin-left: 132px;" placeholder="请输入内容" v-model="input3" class="input-with-select">
          <el-button style="background-color: #f58c0c;color: white;font-size: 15px" slot="append"  icon="el-icon-search">搜索</el-button>
        </el-input>
        <el-button style="margin-left:10px;background-color: #ED6C3E;color: white;font-size: 15px" slot="append"  icon="el-icon-goods">购物车</el-button>
        <div class="logo" style="float: right"><img style="width: 100%" src="https://img13.360buyimg.com/babel/jfs/t1/192532/18/31574/14301/63aeb38dF5c55c212/38245c8dbdee113c.jpg.avif"></div>
      </div>
    </div>
    <div class="sort_and_images">
      <div class="wide">
        <div class="sandi_aside">
          <el-menu :active-text-color="fff" :default-active="activeIndex" class="el-menu-demo" mode="vertical" @select="handleSelect">
            <el-menu-item index="1"><a href="https://www.ele.me" target="_blank">1</a></el-menu-item>
            <el-menu-item index="2"><a href="https://www.ele.me" target="_blank">2</a></el-menu-item>
            <el-menu-item index="3" ><a href="https://www.ele.me" target="_blank">3</a></el-menu-item>
            <el-menu-item index="4"><a href="https://www.ele.me" target="_blank">4</a></el-menu-item>
          </el-menu>
        </div>
        <div class="sandi_images">
          <el-carousel height="475px" :interval="5000" arrow="always">
            <el-carousel-item v-for="item in 4" :key="item">
            </el-carousel-item>
          </el-carousel>
        </div>
      </div>
    </div>

    </div>
  </div>
</template>

<script>
import TopNavigator from '@/components/TopNavigator'
export default {
  name: 'HelloWorld',
  components: { TopNavigator },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  background-color: #f4f4f4;
}
.el-header, .el-footer {
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #D3DCE6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #E9EEF3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}
.wide{
  margin: auto;
  width: 1190px;
}
.search_and_cart{
  background: #fff;
  border-bottom: 1px solid #ddd;
  margin-bottom: 10px;
}
.search_and_cart .wide{
  position: relative;
  z-index: 11;
  height: 140px;
}
.logo{
  overflow: hidden;
  display: flex;
  align-items: center;
  margin: 10px 0px 0px 0px;
  width: 190px;
  height: 120px;
}
.sort_and_images{
  height: 485px;
  background-color: #f4f4f4;
  padding-top: 10px;
  padding-bottom: 10px;
}
.sandi_aside{
  position: relative;
  float: left;
  height: 475px;
  width: 190px;
  margin-right: 15px;
  background-color: #fff;
}
.sandi_images{
  float: left;
  height: 475px;
  width: 975px;
  background-color: #fff;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n+1) {
  background-color: #d3dce6;
}
</style>
