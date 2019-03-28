<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-iconfont">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题</div>
        <div class="header-right">城市
            <span class="iconfont arrow-iconfont">&#xe64a;</span>
        </div>
    </div>
</template>
<script>
export default {
    name:'HomeHeader'
}
</script>
<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .header
        line-height:.86rem
        display:flex
        background: $bgColor
        color:#fff
        .header-left
            width: .64rem
            float:left
            .back-iconfont
                text-align:center
                font-size:.4rem
        .header-input
            flex:1
            background: #fff
            border-radius:.1rem
            height: .64rem
            line-height: .64rem
            margin-top:.12rem
            padding-left:.2rem
            color:#ccc
        .header-right
            width: 1.24rem
            float:right
            text-align: center
            .arrow-iconfont
                font-size:.24rem
                margin-left:-.04rem
</style>




