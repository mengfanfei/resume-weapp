<template>
  <view class="index">
    <swiper class="height100vh">
      <swiper-item class="photo-item">
        <scroll-view class="height100vh">
          <image 
            :src="person" 
            mode="aspectFill" 
            class="photo-image"
          />
          <view class="name">
            孟凡非
          </view>
          <view class="right">
            我的简历 >
          </view>
          <!-- 彩色气泡 -->
          <!-- <view class="big-circle" />
          <view class="mid-circle" />
          <view class="small-circle" /> -->

          <view class="intro">
            <view class="job">
              前端开发工程师
            </view>
            <view class="exp">
              一年工作经验
            </view>
          </view>
        </Scroll-view>
      </swiper-item>
      <swiper-item>
        <scroll-view class="height100vh">
          123
        </scroll-view>
      </swiper-item>
    </swiper>
  </view>
</template>

<script>

export default {
  name: 'Index',
  components: {},
  data() {
    return {
      person: require('../../images/person.jpg').default
    }
  }
}
</script>

<style lang="scss">
.height100vh {
  height: 100vh;
}
.index {
  .photo-item {
    position: relative;
    .photo-image {
      height: 100vh;
      width: 100vw;
    }
    .name {
      position: absolute;
      top: 80px;
      left: 60px;
      font-size: 52px;
      font-weight: bold;
      letter-spacing: 10px;
    }
    .right {
      position: absolute;
      right: 30px;
      top: 80px;
      letter-spacing: 10px;
    }
    .big-circle {
      background-color: rgba(255, 0, 0, 0.8);
      width: 500px;
      height: 500px;
      border-radius: 50%;
      position: absolute;
      left: -300px;
      top: 180px;
    }
    .mid-circle {
      background-color: rgba(255, 0, 0, 0.8);
      width: 300px;
      height: 300px;
      border-radius: 50%;
      position: absolute;
      right: -200px;
      top: 180px;
    }
    .small-circle {
      background-color: rgba(255, 0, 0, 0.8);
      width: 100px;
      height: 100px;
      border-radius: 50%;
      position: absolute;
      right: 0px;
      bottom: 180px;
    }
    .intro {
      position: absolute;
      bottom: 260px;
      background: rgba($color: #000000, $alpha: 0.5);
      text-align: center;
      width: 100%;
      padding: 40px 0;
      color: #ffffff;
      .job {
        font-size: 52px;
        font-weight: bold;
      }
      .exp {
        padding-top: 10px;
        font-weight: normal;
        font-size: 36px;
      }
    }
  }
}
</style>
