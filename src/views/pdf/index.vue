<template>
  <div class="app-container">
    <aside style="margin-top:15px;">{{ $t('pdf.tips') }}</aside>
    <router-link target="_blank" to="/pdf/download">
      <el-button type="primary">
        Click to download PDF
      </el-button>
    </router-link>
    <aside style="margin-top:15px;">pdf</aside>
    <aside style="margin-top:15px;">video</aside>
    <video
      ref="video"
      controls
      src="https://vkceyugu.cdn.bspapp.com/VKCEYUGU-learning-vue/52d32740-aecd-11ea-b244-a9f5e5565f30.mp4">
    </video>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  mounted() {
    this.$nextTick(() => {
      let myVideo = this.$refs.video
      // console.dir(myVideo)
      // 让视频观看到第10s
      myVideo.currentTime = 10;
      //获取视频的总长度
      // console.log(myVideo.duration)
    })
  }
}
</script>

<style scoped>
  video {
    width: 100%;
    height: 100%;
  }
</style>

