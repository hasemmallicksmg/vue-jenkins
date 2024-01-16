<template>
   <div>
    <h1>
        Image Slider with vue swiper awesome swiper  
    </h1>
    <div>
        <ImageSliderThree/>
    </div>
   </div>

</template>
<script>
import ImageSlider from './components/ImageSlider.vue';
import ImageSliderTwo from './components/ImageSliderTwo.vue';
import ImageSliderThree from "./components/ImageSlider3DEffect.vue"

export default {
    components: {
        ImageSlider, ImageSliderTwo,  ImageSliderThree
    }
}
</script>