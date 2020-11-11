<template>
  <div class="page-home">
    <header class="index-header">
      <a href="mine.html?cpid=0">
        <div class="header-user">
          <div class="user-btn"></div>
        </div>
      </a>
      <div class="header-logo"></div>
      <a href="search.html?cpid=0">
        <div class="header-search"></div>
      </a>
    </header>
    <swiper :autoplay = "2000" :loop="true" @change = "changeHandler">
      <SwiperItem>1</SwiperItem>
      <SwiperItem>2</SwiperItem>
      <SwiperItem>3</SwiperItem>
      <SwiperItem>4</SwiperItem>
    </swiper>
  </div>
</template>
<script>
// 引入抽离出的插件
import { Swiper, SwiperItem } from '@/components/Swiper'
export default {
  name: 'Home',
  components: {
    Swiper,
    SwiperItem
  },
  methods: {
    changeHandler (payload) {
      console.log('index', payload)
    }
  }
}
</script>

<style lang ='scss' scoped>
.page-home {
  display: flex;
  flex-direction: column;
  height: 100%;
  background: brown;
  .index-header {
    display: flex;
    height: 44px;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    box-sizing: border-box;
    .user-btn {
      height: 25px;
      width: 25px;
      background: url(~@/assets/icon/user-btn.png);
      background-size: 100%;
    }
    .header-logo {
      width: 92px;
      height: 28px;
      background: url(~@/assets/logo.png) no-repeat;
      background-size: 100%;
    }
    .header-search {
      width: 25px;
      height: 25px;
      background: url(~@/assets/icon/icon-search.png) no-repeat;
      background-size: 100%;
    }
  }
}
</style>
