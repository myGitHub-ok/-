<template>
    <div>
        <view>
            <Swiper :images="images" />
        </view>
        <h3 class="move" @click="goactivity()">热门活动</h3>
        <ul class="text">
            <li>5108</li>
            <li>测试一</li>
        </ul>
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
        goactivity(){
            wx.redirectTo({
                url: '../activity/main'
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
.move{
    padding: 2% 0 2% 1%;
    margin-top: 5%;
    font-weight: 700%;
}
.text>li{
    color: darkgrey;
    padding: 2% 0 2% 1%;
    border-bottom: 1px solid #eeeeee;
    border-top: 1px solid #eeeeee;
}
</style>