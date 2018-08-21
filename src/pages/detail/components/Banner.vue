<template>
    <div>
        <div class="banner"  @click="handleBannerClick">
            <img class="banner-img" src="http://img1.qunarzz.com/sight/p32/201211/09/d24abcc97581ee8b93835fbb.jpg_600x330_1f0c67f7.jpg">
            <div class="banner-info">
                <div class="banner-title">
                    万鸟岛
                </div>
                <div class="banner-number">
                    <span class="iconfont banner-icon">&#xe692;</span>
                    39
                </div>
            </div>
        </div>
        <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
    </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
    export default {
        name:'DetailBanner',
        components: {
            CommonGallary
        },
        data () {
           return {
                imgs: ['http://img1.qunarzz.com/sight/p0/1611/c7/c7e3e61bbe91ffd0a3.water.jpg_350x240_688eb870.jpg','http://img1.qunarzz.com/sight/p0/1611/c7/c7e3e61bbe91ffd0a3.water.jpg_350x240_688eb870.jpg'],
                showGallary:false
           }
        },
        methods: {
            handleBannerClick () {
                this.showGallary=true
            },
            handleGallaryClose () {
                this.showGallary=false
            }
        }
    }
</script>

<style lang="stylus" scoped>
    .banner
        position: relative
        overflow:hidden
        height:0
        padding-bottom: 55%
        .banner-img
            width: 100%
        .banner-info
            display: flex
            position: absolute
            left: 0
            right: 0
            bottom: 0
            line-height: .6rem
            color: #fff
            background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0 ,0.8))
            .banner-title
                font-size: .32rem
                flex: 1
                padding: 0 .2rem
             .banner-number 
               padding: 0 .4rem
               height: .32rem
               line-height: .32rem
               margin-top: .14rem
               border-radius: .2rem
               background: rgba(0, 0, 0, .8)
               font-size: .24rem
               .banner-icon
                   font-size: .24rem 
</style>