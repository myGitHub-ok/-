<template>
    <div>
        <view>
            <Swiper :images="images" />
        </view>
        <div class="sp-tt">
            <div>
                <img src="../../../static/images/cbd.jpg" alt="cd">
                <p @click="gomove()">活动</p>
            </div>
            <div>
                <img src="../../../static/images/muwu.jpg" alt="me">
                <p>问卷</p>
            </div>
            <div>
                <img src="../../../static/images/shuijiao.jpg" alt="to">
                <p>夏令营</p>
            </div>
            <div>
                <img src="../../../static/images/yuantiao.jpg" alt="taek">
                <p>课程</p>
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
      gomove(){
        wx.redirectTo({
          url: '../move/main'
        })
      }
    };
  },
  methods: {

  }
};
</script>

<style>
.message {
  color: red;
  padding: 10px;
  text-align: center;
}
.sp-tt{
    width: 100%;
    /* height: 100%; */
    display: flex;
    flex-wrap: wrap;
}
.sp-tt>div{
    width: 45%;
    margin-top: 5%;
    margin-left: 1%;
    margin-right: 1%;
    padding: 1% 1%;
    border: 1px solid #999;
}
.sp-tt>div img{
    width: 100%;
}
.sp-tt>div p{
    text-align: center;
}
</style>