<template>
    <div>
        <view>
            <Swiper :images="images" />
        </view>
        <div class="ybm-dv">
            <ul>
                <li>
                    <p>2</p>
                    <h5>已报名</h5>
                </li>
                <li>
                    <p>0</p>
                    <h5>总投票</h5>
                </li>
                <li>
                    <p>355</p>
                    <h5>浏览量</h5>
                </li>
            </ul>
        </div>
        <div class="bm-h3">
            <h3 @click="goenroll()">我要报名</h3>
        </div>
        <div class="js-p">
            <p>距离活动结束：40天15时13分37秒</p>
        </div>
        <div class="sou-int">
            <input type="text" placeholder="姓名">
            <button>搜索</button>
        </div>
        <div class="fz-btn">
            <button>选择分组</button>
        </div>
        <div class="fool-dv">
            <div class="fool-dva">
                <img src="../../../static/images/s8.jpg" alt="手机">
                <p @click="gopag()">啦啦啦</p>
                <p>0票</p>
                <button>投票</button>
            </div>
            <div class="fool-dvb">
                <img src="../../../static/images/s8.jpg" alt="手机">
                <p>嘿嘿嘿</p>
                <p>0票</p>
                <button>投票</button>
            </div>
        </div>
        <div class="fol-fol">
            <div class="fol-ftx">
                <p>已经到底部啦！</p>
            </div>
            <div class="fol-img">
                <img src="../../../static/images/0413f6b9b7d0ceddbf35b6eec1a8e93b.png" alt="你的名字">
            </div>
        </div>
    </div>
</template>

<script>
import Swiper from "@/components/swiper";


export default {
  components: { Swiper },
  data() {
    return {
      images: [
        {
          url:
            "https://img-oss.yunshanmeicai.com/goods/default/31d8dfa4-0d7b-4694-80f9-41b07c9d0a3a.png"
        },
        {
          url:
            "https://img-oss.yunshanmeicai.com/goods/default/e83c8f0f-4acc-4729-bcbb-294f2b314977.jpg"
        }
      ],
      gopag(){
        wx.redirectTo({
            url: '../pag/main'
        })
      },
      goenroll(){
         wx.redirectTo({
            url: '../enroll/main'
        }) 
      }
    };
  },
  methods: {

  }
};
</script>

<style scoped>
.message {
  color: red;
  padding: 10px;
  text-align: center;
}
.ybm-dv{
    width: 93%;
    margin: 0 auto;
    background-color: aquamarine;
    color: #ffffff;
    overflow: hidden;
    margin-top: 5%;
}
.ybm-dv ul li{
    float: left;
    width: 31%;
    text-align: center;
    padding: 5% 0;
}
.bm-h3{
    width: 80%;
    margin: 0 auto;
}
.bm-h3 h3{
    margin: 14% 0;
    background-color: aquamarine;
    border-radius: 5%;
    color: #ffffff;
    text-align: center;
    padding: 3% 0;
}
.js-p{
    width: 93%;
    border: 1px solid rgb(235, 233, 233);
    padding: 1% 0;
    margin: 0 auto;
    text-align: center;
}
.sou-int{
    width: 93%;
    margin: 0 auto;
    margin-top: 5%;
    overflow: hidden;
}
.sou-int>input{
    width: 70%;
    height: 40px;
    border: 1px solid rgb(235, 233, 233);
    float: left;
    box-sizing: border-box;
    vertical-align:middle;
    padding-left: 1%;
}
.sou-int>button{
    width: 30%;
    height: 40px;
    float: left;
    box-sizing: border-box;
    background-color: aquamarine;
    text-align: center;
    line-height: 40px;
    color: #ffffff;
}
.fz-btn{
    width: 30%;
    height: 30px;
    margin-top: 5%;
}
.fz-btn button{
    background-color: aquamarine;
    text-align: center;
    line-height: 30px;
    margin-left: 10%;
}
.fool-dv{
    width: 93%;
    display: flex;
    flex-direction: row;
    margin-top: 5%;
}
.fool-dv .fool-dva,.fool-dv .fool-dvb{
    width: 50%;
}
.fool-dv .fool-dva img,.fool-dv .fool-dvb img{
    width: 100%;
}
.fool-dva p,.fool-dvb p{
    padding: 10rpx 0 10rpx 40rpx;
}
.fool-dva button,.fool-dvb button{
    width: 70%;
    margin-top: 10rpx;
    background-color: aquamarine;
    color: #ffffff;
}
.fol-fol{
    width: 100%;
    height: 500rpx;
    display: flex;
    flex-wrap: wrap;
}
.fol-ftx{
    width: 100%;
    height: 250rpx;
    text-align: center;
    line-height: 250rpx;
}
.fol-img{
    width: 100%;
    height: 250rpx;
}
.fol-img img{
    width: 100%;
    height: 100%;
}
</style>