<template>
    <div>
        <div class="title">
            <h2>母婴咨询</h2>
        </div>
        <div class="cont">
            <div class="item">
                <img src="../img/hot5.jpg" alt="">
                <div>
                    <h3 class="item-title">宝宝咨询</h3>
                    <span class="item-time">2019-4-1</span>
                    <span class="item-text">哪些胎教观念是错误的?胎教对于胎儿发育有着积极的作用，因此孕期如果条件允许的话，你可以给孩子进行一些音乐胎教，阅读胎教还有一些运动胎教!但是对于胎教，你不可忽视以下几个错误的观念，不然会对母婴健康造成不利哦!

“胎教是没有严格的生理学研究基础的，不利于胎儿正常的生长发育。”——儿童保健专家丁宗一教授，在联合国儿童基金会召开的《儿童有权拥有最佳人生开端》专题报告会上如是说。可以说是对所谓胎教提出了批评性的意见。</span>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{}
    }
}
</script>
<style scoped>
.title{
    width: 1200px;
    text-align: center;
    margin:0 auto;
    padding:60px 0;
}
h2{
    font-weight: 400;
}
.cont{
    width: 1200px;
    margin: 0 auto;
    padding:0 100px;
}
.item{
    border:1px solid #e2e2e2;
    border-radius: 20px;
    display: flex;
}
.item img{
    border-radius: 20px;
}
.item span{
    display: block;
    padding: 20px;
}
.item h3{
    display: block;
    padding: 20px;
    margin: 0;
}
.item .item-text{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    width: 648px;
}
a{
    text-decoration: none !important;
}
</style>
