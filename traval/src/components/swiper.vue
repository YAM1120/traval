<template>
    <div class="wrap">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item in imgList" :key="item.id">
                <img alt="" class="swiper-img" :src="item.imgsrc">
            </swiper-slide>
        <!-- <div class="swiper-pagination" slot="pagination"></div>  -->
        </swiper>
        <div class="swiper-pagination" slot="pagination"></div> 
    </div>
</template>
<script>
export default {
    name:"homeswiper",
    data(){
        return{
            swiperOption: {//swiper3
            autoplay: 3000,
            speed: 1000,
            loop:true,
            pagination:'.swiper-pagination'
            },
             imgList:[
            {
                id:0,
                imgsrc:'//imgs.qunarzz.com/vs_ceph_vcimg/b8c4527c41649814cc4cf86880abba54.jpeg'
            },
            {
                id:1,
                imgsrc:'//imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg'
            },
            {
                id:2,
                imgsrc:'//imgs.qunarzz.com/vc/6d/9f/35/b8ad5468f73fd60ec0ced086f6.jpg_92.jpg'
            }
        ]
        }
    }
}
</script>
<style scoped>
    /* >>>表示穿透，即wrap下面的swiper-pagination-bullet-active突破scoped的限制 */
    .wrap >>> .swiper-pagination-bullet-active{
        background: #fff;
    }
    .swiper-pagination{
        top: 2.8rem;
        left: 50%;
        margin-left: -.4rem;
    }
    .wrap{
        /* 防止页面加载时出现抖动感 */
        width: 100%;
        height: 0;
        padding-bottom: 2rem;
        overflow: hidden;
    }
    .swiper-img{
        width: 100%;
    }
</style>