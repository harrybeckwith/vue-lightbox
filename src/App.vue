<template>
  <section>
    <h2>Light box</h2>
    <LightBox
      :thumbnails="lightbox.images.thumbnails"
      :largeImages="lightbox.images.large"
      :thumbnailsPath="lightbox.thumbnailsPath"
      :largePath="lightbox.largePath"
      :captions="lightbox.captions"
      class="lightBox"
    />
    <hr>
  </section>
</template>

<script>
import LightBox from "@/components/LightBox.vue";

export default {
  name: "app",
  data() {
    return {
      lightbox: {
        images: {
          thumbnails: ["1.jpg", "2.jpg", "3.jpg"],
          large: ["1.jpg", "2.jpg", "3.jpg"]
        },
        captions: ["caption 1", "caption 2", "caption 3"],
        thumbnailsPath: "/img/sea/thumbnails/",
        largePath: "/img/sea/large/"
      }
    };
  },
  components: {
    LightBox
  }
};
</script>

<style lang ="scss">
.light-box {
  &__thumbnail {
    margin: 20px;
    width: 200px;
  }
}
img {
  max-width: 100%;
}
</style>
