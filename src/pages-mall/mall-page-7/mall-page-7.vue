<script setup lang="ts">
import { onHide, onShow } from '@dcloudio/uni-app'
import { ref } from 'vue'

const pageTitle = ref('mall-page-7')
const componentTitle = ref('mall 标题 7')
const componentContent = ref('这是第 7 个 mall 页面的简单内容')
const totalPages = ref(150)

function navigateBack() {
  uni.navigateBack()
}

onShow(() => {
  console.log('mall-page-7 页面显示')
})

onHide(() => {
  console.log('mall-page-7 页面隐藏')
})
</script>

<template>
  <view class="page">
    <view class="page-header">
      <text class="page-title">{{ pageTitle }}</text>
      <text class="page-subtitle">这是 mall-page-7 页面</text>
    </view>

    <simple-component
      :title="componentTitle"
      :content="componentContent"
    />

    <view class="page-content">
      <text class="info">页面编号: 7</text>
      <text class="info">分包类型: mall</text>
      <text class="info">总页面: ${totalPages}</text>
    </view>

    <view class="page-footer">
      <button @click="navigateBack">
        返回
      </button>
    </view>
  </view>
</template>

<style scoped>
.page {
  min-height: 100vh;
  background: #f5f5f5;
  padding: 20rpx;
}

.page-header {
  background: #fff;
  padding: 40rpx;
  border-radius: 10rpx;
  margin-bottom: 20rpx;
  text-align: center;
}

.page-title {
  font-size: 36rpx;
  font-weight: bold;
  color: #333;
  display: block;
  margin-bottom: 10rpx;
}

.page-subtitle {
  font-size: 28rpx;
  color: #666;
  display: block;
}

.page-content {
  background: #fff;
  padding: 30rpx;
  border-radius: 10rpx;
  margin: 20rpx 0;
}

.info {
  font-size: 28rpx;
  color: #333;
  display: block;
  margin-bottom: 10rpx;
}

.page-footer {
  display: flex;
  gap: 20rpx;
  margin-top: 40rpx;
}
</style>
