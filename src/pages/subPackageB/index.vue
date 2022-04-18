<template>
  <view class="content">
    分包页面B
    <image class="logo" src="/static/logo.png" @click="routeToPageA"></image>
    <view> 
      <text class="title">{{ title }}</text>
    </view>

    <testCompo/>
  </view>
</template>

<script>
import testCompo from './testComp'

export default {
  data () {
    return {
      title: 'Hello subpackage.B',
    };
  },
  components:{
    testCompo
  },
  onLoad () {
    const app = getApp()
  },
  methods: {
    routeToPageA(){
      wx.navigateTo({
        url:'/pages/subPackageA/index'
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
