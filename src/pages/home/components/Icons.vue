<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" />
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  name: "HomeIcons",
  data () {
    return {
      swiperOption:{
        autoplay:false
      }
    }
  },
  props:{
    list: Array
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item,index) =>{
        const page = Math.floor(index/8)  //算出图片在轮播图的第几页，向下取整为0则在第1页，向下取整为1则在第2页
        if (!pages[page]) {
        pages[page] = []
        }
        pages[page].push(item)
      }) //对iconList中的每一项数据进行循环，循环会接收两个参数，一个是具体的循环项，一个是循环对应的的下标。
      return pages
    }
  }
};
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  
  .icons >>> .swiper-container
    width: 100%
    height: 0
    padding-bottom: 50%
  .icons
    margin-top:.1rem
    .icon 
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-img 
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: 0.44rem
        box-sizing: border-box
        padding: 0.1rem
        .icon-img-content 
          height: 100%
          display: block
          margin: 0 auto
      .icon-desc 
        text-align: center
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: 0.44rem
        line-height: 0.44rem
        color: $darkTextColor
        overflow:hidden
        wrap:nowrap
        text-overflow:ellipsis
</style>
   


