<template>
  <div class="example">
    {{ msg }}
    <video-player :options="videoOptions"/>
  </div>
</template>

<script>
import VideoPlayer from './components/VideoPlayer.vue';

export default {
  components: {
		VideoPlayer
	},
  data () {
    return {
      msg: 'Hello worldu!',
      videoOptions: {
				autoplay: true,
        controls: true,
        width: 800,
        height: 400,
        playbackRates: [0.5, 1, 1.5, 2, 4],
				sources: [
					{
            src: 'file:///',
						type: "video/mp4"
					}
				]
			}
    }
  }
}
</script>

<style>
.example {
  color: red;
}
</style>