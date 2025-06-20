<template>
  <view class="page-wrapper">
    <!-- Fixed Top Search Header -->
    <view class="search-header">
      <text class="title">Search</text>
      <view class="search-bar">
        <text class="icon">
          <img class="icons" src="/static/icons/search-icon.png" />
        </text>
        <input class="input" placeholder="Search cards..." />
      </view>
      <view class="filters">
        <view class="filter">Nearby</view>
        <view class="filter">Popular</view>
        <view class="filter">Eco-Friendly</view>
      </view>
    </view>

    <!-- Scrollable Content -->
    <scroll-view scroll-y class="scroll-area" show-scrollbar="false">
      <view class="container">
        <!-- Featured Collections -->
        <view class="section">
          <view class="section-bar">
            <text class="section-title">
              <img class="icons" src="/static/icons/heart-icon.png" />
              Featured Collections
            </text>
          </view>
          <scroll-view
            scroll-x="true"
            class="horizontal-scroll"
            show-scrollbar="false"
          >
            <view class="card-list">
              <view class="card">
                <image
                  src="/static/cards/paokemon-card.png"
                  class="card-image"
                />
                <text class="card-text">Pokemon Card</text>
              </view>
              <view class="card">
                <image src="/static/cards/nba-card.png" class="card-image" />
                <text class="card-text">NBA Sports Card</text>
              </view>
              <view class="card">
                <image
                  src="/static/cards/paokemon-card.png"
                  class="card-image"
                />
                <text class="card-text">Pokemon Card</text>
              </view>
              <view class="card">
                <image src="/static/cards/nba-card.png" class="card-image" />
                <text class="card-text">NBA Sports Card</text>
              </view>
              <view class="card">
                <image
                  src="/static/cards/paokemon-card.png"
                  class="card-image"
                />
                <text class="card-text">Pokemon Card</text>
              </view>
              <view class="card">
                <image src="/static/cards/nba-card.png" class="card-image" />
                <text class="card-text">NBA Sports Card</text>
              </view>
            </view>
          </scroll-view>
        </view>

        <!-- Market Trends -->
        <view class="section">
          <view class="section-bar">
            <text class="section-title">
              <img class="icons" src="/static/icons/trend-icon.png" /> Market
              Trends
            </text>
          </view>
          <view class="trend-row">
            <view class="trend-card green">
              <text class="trend-title">Pokemon</text>
              <text class="trend-percent">33.79%</text>
              <img class="trend-img" src="/static/icons/green-trend.png" />
            </view>
            <view class="trend-card red">
              <text class="trend-title">Basketball</text>
              <text class="trend-percent">5.79%</text>
              <img class="trend-img" src="/static/icons/red-trend.png" />
            </view>
            <view class="trend-card green">
              <text class="trend-title">Pokemon</text>
              <text class="trend-percent">33.79%</text>
              <img class="trend-img" src="/static/icons/green-trend.png" />
            </view>
            <view class="trend-card red">
              <text class="trend-title">Basketball</text>
              <text class="trend-percent">5.79%</text>
              <img class="trend-img" src="/static/icons/red-trend.png" />
            </view>
            <view class="trend-card green">
              <text class="trend-title">Pokemon</text>
              <text class="trend-percent">33.79%</text>
              <img class="trend-img" src="/static/icons/green-trend.png" />
            </view>
            <view class="trend-card red">
              <text class="trend-title">Basketball</text>
              <text class="trend-percent">5.79%</text>
              <img class="trend-img" src="/static/icons/red-trend.png" />
            </view>
          </view>
        </view>

        <!-- Hot Cards -->
        <view class="section">
          <view class="section-bar">
            <text class="section-title">
              <img class="icons" src="/static/icons/hot-icon.png" /> Hot Cards
            </text>
          </view>
          <view class="hot-card">
            <image src="/static/cards/hot-card.png" class="hot-card-img" />
            <view class="hot-card-info">
              <text class="hot-card-name">Eevee</text>
              <text class="hot-card-price"
                ><img
                  class="dollar-icon"
                  src="/static/icons/dollar-icon.png"
                />355.02</text
              >
            </view>
          </view>
          <view class="hot-card">
            <image src="/static/cards/hot-card.png" class="hot-card-img" />
            <view class="hot-card-info">
              <text class="hot-card-name">Eevee</text>
              <text class="hot-card-price"
                ><img
                  class="dollar-icon"
                  src="/static/icons/dollar-icon.png"
                />355.02</text
              >
            </view>
          </view>
          <view class="hot-card">
            <image src="/static/cards/hot-card.png" class="hot-card-img" />
            <view class="hot-card-info">
              <text class="hot-card-name">Eevee</text>
              <text class="hot-card-price"
                ><img
                  class="dollar-icon"
                  src="/static/icons/dollar-icon.png"
                />355.02</text
              >
            </view>
          </view>
          <view class="hot-card">
            <image src="/static/cards/hot-card.png" class="hot-card-img" />
            <view class="hot-card-info">
              <text class="hot-card-name">Eevee</text>
              <text class="hot-card-price"
                ><img
                  class="dollar-icon"
                  src="/static/icons/dollar-icon.png"
                />355.02</text
              >
            </view>
          </view>
        </view>
      </view>
    </scroll-view>

    <!-- Fixed Bottom Navigation -->
    <Footer />
  </view>
</template>

<script setup>
import Footer from "@/components/Footer.vue"; // adjust path as needed
</script>
<style scoped>
.page-wrapper {
  height: 100vh;
  display: flex;
  flex-direction: column;
  position: relative;
  background: #1a0033;
}

/* Fixed Top Header */
.search-header {
  position: fixed;
  margin: 50rpx 20rpx 0 0;
  width: 90%;
  background: #1a0033;
  z-index: 20;
  padding: 30rpx;
  color: white;
}

.search-header .title {
  font-size: 48rpx;
  margin-bottom: 20rpx;
}

.search-bar {
  display: flex;
  align-items: center;
  background: #2a0044;
  border-radius: 20rpx;
  padding: 10rpx 20rpx;
  margin-bottom: 20rpx;
  height: 52px;
  margin-top: 20rpx;
}

.icon {
  margin-right: 10rpx;
}

.input {
  flex: 1;
  color: white;
  background: transparent;
  border: none;
}

.filters {
  display: flex;
  gap: 20rpx;
  margin-bottom: 10rpx;
  color: white;
}

.filter {
  padding: 10rpx 20rpx;
  border: 2rpx solid #8a4dff;
  border-radius: 30rpx;
  font-size: 19px;
  height: 25px;
  line-height: 25px;
}

/* Scrollable Area */
.scroll-area {
  margin-top: 280rpx; /* space for fixed header */
  margin-bottom: 160rpx; /* space for fixed footer */
  flex: 1;
  overflow-y: scroll;
}

/* Content Container */
.container {
  color: #fff;
  padding: 0 30rpx 100rpx;
}

.section {
  margin-bottom: 10%;
}

.section-bar {
  margin-bottom: 15px;
}

.section-title {
  font-size: 36rpx;
}

/* Cards */
.horizontal-scroll {
  white-space: nowrap;
  overflow-x: scroll;
  display: flex;
  margin-top: 10%;
}

.card-list {
  display: flex;
  flex-direction: row;
  gap: 15%;
  padding: 10rpx 0;
}

.card {
  flex-shrink: 0;
  width: 240rpx;
  position: relative;
}

.card-image {
  width: 170px;
  height: 216px;
  border-radius: 20rpx;
  display: block;
}

.card-text {
  position: absolute;
  bottom: 10%;
  left: 50%;
  transform: translateX(-50%);
  background: rgba(0, 0, 0, 0.3);
  padding: 6rpx 12rpx;
  border-radius: 12rpx;
  font-size: 26rpx;
  color: #fff;
  white-space: nowrap;
  text-align: center;
}

/* Trends */
.trend-row {
  display: flex;
  gap: 20rpx;
  overflow-x: auto;
  padding-bottom: 10rpx;
  scroll-snap-type: x mandatory;
}

.trend-card {
  flex: 0 0 auto;
  width: 260rpx;
  padding: 20rpx;
  border-radius: 20rpx;
  background: #2a0044;
  scroll-snap-align: start;
}

.green {
  color: #00ff7f;
}

.red {
  color: #ff4444;
}

.trend-img {
  margin-top: 10rpx;
  width: 50px;
  height: 17.5px;
}

/* Hot Cards */
.hot-card {
  display: flex;
  align-items: center;
  background: #2a0044;
  border-radius: 20rpx;
  padding: 20rpx;
  margin-top: 20rpx;
}

.hot-card-img {
  width: 100rpx;
  height: 100rpx;
  border-radius: 10rpx;
  margin-right: 20rpx;
}

.hot-card-info {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

/* Footer */
.bottom-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 100rpx;
  background: #2a0044;
  display: flex;
  justify-content: space-around;
  align-items: center;
  z-index: 10;
  padding-bottom: 60rpx;
  border-top-left-radius: 50px;
  border-top-right-radius: 50px;
}

.icons {
  height: 16px;
  width: 16px;
}
.dollar-icon {
  height: 16px;
  width: 16px;
  margin: 0px 5px;
}
</style>
