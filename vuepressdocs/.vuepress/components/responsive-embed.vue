<template>
    <div class="video-responsive">
        <iframe max-width=100% height=auto :src="source" frameborder="0" allow="encrypted-media" allowfullscreen></iframe>
    </div>
</template>

<script>
export default {
  name: 'responsive-embed',
   props: {
     source: {
       type: String,
       required: true,
     }
   }
}
</script>

<style scoped lang='stylus'>

.video-responsive {
  position: relative; 
  padding-bottom: 56.25%; /* 16:9 */
  height: 0;
  overflow: hidden;
  width: 100%; height: auto;
  margin-top: 40px;
  margin-bottom: 40px;
}

.video-responsive iframe {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
}
</style>
