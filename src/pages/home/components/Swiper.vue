<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://img1.qunarzz.com/p/tts9/1704/6e/797e073f945f1f02.jpg_r_640x420x90_2106ae24.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/p/tts9/1705/50/afcfb325f9a6f002.jpg_r_640x420x90_b44c4b77.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper <<< .swiper-pagination-bullet-active
  background: #ffffff
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 31.25%
  background: #eeeeee
  .swiper-img
    width: 100%
</style>
