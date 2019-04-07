<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: "HomeSwiper", //组件的名称
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination",
        loop: true
      },
      swiperList: [
        {
          id: "0001",
          imgUrl:
            "https://img1.qunarzz.com/vc/2a/96/76/d149c7a3a5b113f876f9a66e09.png"
        },
        {
          id: "0002",
          imgUrl:
            "https://img1.qunarzz.com/vc/bf/9d/a3/67b7b37511fa26a78298bf1da1.jpg"
        },
        {
          id: "0003",
          imgUrl:
            "https://img1.qunarzz.com/vc/b8/25/51/f6173dbd12c1a0f783abe73855.jpg"
        },
        {
          id: "0004",
          imgUrl:
            "https://img1.qunarzz.com/vc/80/80/1a/72b8f423c33e581ca72fc136da.jpg"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #ccc;
}

.wrapper {
  width: 100%;
  height: 31.25vw;
  background: #eee;

  .swiper-img {
    width: 100%;
  }
}
</style>

