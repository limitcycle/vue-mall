<template>
  <div>
    <Carousel />
    <GoodsList />
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from '@/components/Carousel.vue'
import GoodsList from '@/components/GoodsList.vue'

export default {
  name: 'Home',
  components: { Carousel, GoodsList }
}
</script>
