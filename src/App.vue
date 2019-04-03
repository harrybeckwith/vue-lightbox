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
    <Accordion :accordionItems="accordion"/>
  </section>
</template>

<script>
import LightBox from "@/components/LightBox.vue";
import Accordion from "@/components/Accordion.vue";
export default {
  name: "app",
  data() {
    return {
      lightbox: {
        images: {
          thumbnails: ["1.jpg", "2.jpg", "3.jpg"],
          large: ["1.jpg", "2.jpg", "3.jpg"]
        },
        captions: ["caption 1", "cap 2", "caption 3"],
        thumbnailsPath: "/img/sea/thumbnails/",
        largePath: "/img/sea/large/"
      },
      accordion: [
        {
          title: "title one",
          content: "content example here",
          active: true
        },
        {
          title: "title two",
          content: "content example here",
          active: false
        },
        {
          title: "title three",
          content: "content example here",
          active: false
        }
      ]
    };
  },
  components: {
    LightBox,
    Accordion
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
