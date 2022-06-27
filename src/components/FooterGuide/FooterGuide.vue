<template>
   <div class="footer_guide">
     <!-- 类名确定,只是不确定有没有这个类名   on:'/msite'当前路径 === $route.path请求的路径-->
     <a href="javascript:;" class="guide_item" :class="{on:'/msite' === $route.path}" @click="goTo('/msite')">
       <span class="item_icon">
         <i class="iconfont icon-u"></i>
       </span>
       <span>外卖</span>
     </a>
     <a href="javascript:;" class="guide_item" :class="{on:'/search' === $route.path}" @click="goTo('/search')">
       <span class="item_icon">
         <i class="iconfont icon-sousuo"></i>
       </span>
       <span>搜索</span>
     </a>
     <a href="javascript:;" class="guide_item" :class="{on:'/order' === $route.path}" @click="goTo('/order')">
       <span class="item_icon">
         <i class="iconfont icon-dingdan"></i>
       </span>
       <span>订单</span>
     </a>
     <!-- 通过动态 class 和$route.path 来实现 tab 样式切换 -->
     <a href="javascript:;" class="guide_item" :class="{on:'/profile' === $route.path}" @click="goTo('/profile')">
       <span class="item_icon">
         <i class="iconfont icon-geren1 "></i>
       </span>
       <span>我的</span>
     </a>
   </div>
 
</template>

<script>
export default {
  name: '',

  data () {
    return {
    }
  },

  methods: {
    goTo(path){
      this.$router.replace(path)
    }
  }
}
</script>

<style lang='stylus' rel='stylesheet/stylus'>
@import "../../common/stylus/mixins.styl";
.footer_guide
  top-border-1px(#e4e4e4)
  position: fixed
  z-index 100
  left: 0
  right: 0
  bottom: 0
  background-color #fff
  width 100%
  height 50px
  display: flex
  .guide_item
    display: flex
    flex: 1
    text-align: center
    flex-direction: column
    align-items: center
    margin 5px
    color: #999
    &.on
      color: #02a774
    span  
      font-size:14px
      margin-top  2px
      margin-bottom 2px
      .iconfont
        font-size: 22px

  </style>
