<template>
<div class="wrappper">
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default {
    name: 'HomeSwiper',
    data() {
        return {
            swiperOptions: {
              pagination: {
                el: '.swiper-pagination',
                loop: true    // 貌似无效
              }
            },
            swiperList: [{
              id: '001',
              imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/3ccfc3d5bd540a537ebfbd8a08649900.jpeg'
            },  {
              id: '002',
              imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/c19d77cffc63cce31dcd336c7879fc1d.jpeg'
            },  {
              id: '003',
              imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/06159c91f87c2cfbecd9294f93fff700.jpeg'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .wrappper
      overflow: hidden
      width: 100%
      height: 0
      padding-bottom: 27.08%
      background-color: #eee
      .swiper-img
        width: 100%
</style>>
