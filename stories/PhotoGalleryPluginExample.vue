<template>
<div>
  <div class="title">Using as a Plugin</div>
  <a v-for="(image, index) in images" class="thumb-item" href="#" @click="openGallery(index)">
    <img :src="image.thumbSrc"/>
  </a>
</div>
</template>

<script>
export default {
  name: "PhotoGalleryPluginExample",
  data() {
    return {
      images: [
        {
          src:
            "https://farm4.staticflickr.com/3894/15008518202_c265dfa55f_h.jpg",
          thumbSrc:
            "https://farm4.staticflickr.com/3894/15008518202_b016d7d289_m.jpg",
          w: 1600,
          h: 1600
        },
        {
          src:
            "https://farm6.staticflickr.com/5591/15008867125_b61960af01_h.jpg",
          thumbSrc:
            "https://farm6.staticflickr.com/5591/15008867125_68a8ed88cc_m.jpg",
          w: 1600,
          h: 1068
        },
        {
          src:
            "https://farm4.staticflickr.com/3902/14985871946_24f47d4b53_h.jpg",
          thumbSrc:
            "https://farm4.staticflickr.com/3902/14985871946_86abb8c56f_m.jpg",
          w: 1600,
          h: 1067
        }
      ],
      visiblePhoto: null
    };
  },
  methods: {
    openGallery(index) {
      this.$photoGallery.open(index, this.images);
    }
  }
};
</script>

<style lang="css" scoped>
  .title {
    margin-bottom: 10px;
    font-size: 1.3em;
  }
</style>
