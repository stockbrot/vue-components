<template>
  <v-carousel hide-delimiters hide-controls>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="`https://unsplash.it/1080/300?image=${Math.floor(Math.random() * 100) + 1}`"
    >
      <v-layout
        align-start
        justify-center
        column
        fill-height
      >
        <div class="custom-caption pa-4 display-1">
          <h4>{{ item.header }}</h4>
        </div>
      </v-layout>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  name: 'CarouselComp',
  props: {
    items: Array
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="stylus">
.carouselcomp
  width 100%
.custom-caption
  text-align center
  padding 12px
  color white
  text-shadow 2px 2px rgba(0,0,0,0.4)
</style>
