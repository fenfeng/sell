<template>
    <div class="header">
        <div class="content-wrapper">
            <div class="avatar">
                <img width="64" height="64" :src="seller.avatar">
            </div>
            <div class="content">
                <div class="title">
					<span class="brand"></span>
                    <span class="name">{{seller.name}}</span>
                </div>
                <div class="description">
                    {{seller.description}}/{{seller.deliveryTime}}分钟送达
                </div>
                <div v-if="seller.supports" class="support">
                    <span class="icon"></span>
                    <span class="text">{{seller.supports[0].description}}</span>
                </div>
            </div>
        </div>
        <div class="bulletin-wrapper"></div>
    </div>
</template>

<script type="text/javascript">
    export default{
        props: {
            seller: {
                type: Object
            }
        }
    };
</script>

<style lang="stylus" rel="stylesheet/stylus">
    .header
        color : #fff
        backgournd : #000
        .content-wrapper
            padding: 24px 12px 18px 24px
            .avatar
                display: inline-block
            .content
                display: inline-block
                .title
                    margin: 2px 0 8px 0
                    .brand
                        display inline-block
                        vertical-align top
                        width 30px
                        height 18px
                        bg-image('brand')
                        background-size 30px 18px
                        background-repeat no-repeat
</style>