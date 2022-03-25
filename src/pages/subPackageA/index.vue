<template>
  <view class="content">
    分包页面A
    <image class="logo" src="/static/logo.png" @click="routeToPageB"> </image>
    <view>
      <text class="title">{{ title }}</text>
    </view>
  </view>
</template>

<script>

export default {
  data () {
    return {
      title: 'Hello subpackage.A',
    };
  },
  onLoad () {

  },
  methods: {
    routeToPageB(){
      wx.navigateTo({
        url:'/pages/subPackageB/index'
      })
    }
  },
};
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin: 200rpx auto 50rpx auto;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style>
