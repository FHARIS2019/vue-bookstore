<template>
  <div class="mt-3">
    <b-carousel id="my-carousel"
                style="text-shadow: 1px 1px 2px #333;"
                controls
                indicators
                background="#555"
                :interval="4000"
                v-model="slide"
                img-height="250px"
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
    >
      <b-carousel-slide img-blank img-width="780px" img-height="250px" caption="Immense">
        <p>
          Huge collection of books both classics and recent.
        </p>
      </b-carousel-slide>

      <b-carousel-slide img-blank img-width="780px" img-height="250px" caption="Aesthetic">
        <p>
          Best qualilty priting, every page matters to us!
        </p>
      </b-carousel-slide>

      <b-carousel-slide img-blank img-width="780px" img-height="250px" caption="Faster">
        <p>
          Fastest delivery for your favorite boook
        </p>
      </b-carousel-slide>

    </b-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      slide: 0,
      sliding: null
    }
  },
  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  }
}
</script>

<style scoped>
  #my-carousel {
    margin-top: auto;
  }
</style>
