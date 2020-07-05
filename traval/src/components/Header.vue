<template>
    <div class="header">
        <div class="header-left">
            <img class="left" src="../assets/imgs/left.svg" />
        </div>
        <div class="header-mid">
            <img class="search" src="../assets/imgs/search.svg" />
            <input class="input" placeholder="请输入关键字" />
        </div>
        <div class="header-right">
            <!-- 城市 -->
            <img class="down" src="../assets/imgs/down.svg" />
        </div>
    </div>
</template>
<script>
export default {
    name:"Header"
}
</script>
<style scoped>
    .header{
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 100%;
        height: 1.2rem;
        background: #00bcd4;
        line-height: 1.2rem;
    }
    .header-mid{
        position: relative;
        margin-left: .5rem;
    }
    .search{
        position: absolute;
        left: .1rem;
        top: .35rem;
        width: .5rem;
        height: .5rem;
    }
    .input{
        width: 5rem;
        height: .8rem;
        border-radius: .2rem;
        padding-left: .6rem;
    }
    .left{
        width: .5rem;
        height: .5rem;
        float: left;
        margin-left: .2rem;
        }
        .down{
            width: .5rem;
            height: .5rem;
            float: right;
        }

</style>