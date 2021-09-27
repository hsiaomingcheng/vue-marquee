<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <swiper
    :slides-per-view="1"
    @swiper="onSwiper"
    @slideChange="onSlideChange"
  >
    <swiper-slide class="box red">Slide 1</swiper-slide>
    <swiper-slide class="box blue">Slide 2</swiper-slide>
    <swiper-slide class="box pink">Slide 3</swiper-slide>
  </swiper>
</template>

<script>
import { reactive } from 'vue';

import { Autoplay } from 'swiper';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import "swiper/swiper.min.css";

export default {
  name: 'App',
  components: {
    Swiper,
    SwiperSlide
  },
  setup() {
    const swiper_options = reactive({
      
    })

    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log('slide change');
    };

    return {
      onSwiper,
      onSlideChange,
    };
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 60px;
}

.box {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 50px;
}
.red {
  background: red;
}
.blue {
  background: blue;
}
.pink {
  background: pink;
}
</style>
