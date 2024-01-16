<template>
    <div class="cube-example" style="height: 400px; width: 400px;">
      <swiper
        class="swiper"
        :modules="modules"
        :navigation="false"
        :pagination="true"
        :effect="'cube'"
        :grab-cursor="true"
       
      >
        <swiper-slide class="slide" v-for="(image, i) in images" :key="i">
          <img :src="image" style="height: 400px;" />
        </swiper-slide>
      </swiper>
    </div>
  </template>
  
  <script>
  import { ref } from "vue";
  import { Swiper, SwiperSlide } from "vue-awesome-swiper";
  import SwiperClass, { Pagination, EffectCube, Navigation } from "swiper";
  
  // import swiper module styles
  import "swiper/css";
  import "swiper/css/pagination";
  import "swiper/css/effect-cube";
  import "swiper/css/navigation";
  
  
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
        const modules = ref([Pagination, EffectCube, Navigation]);
        
        // Your array of image URLs
        const images = ref([
          "https://images.pexels.com/photos/772803/pexels-photo-772803.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
         "https://images.pexels.com/photos/417074/pexels-photo-417074.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2",
        ]);
  
      return {
        modules,
        images,
      };
    },
  };
  </script>
  
