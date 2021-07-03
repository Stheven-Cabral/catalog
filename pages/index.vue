<template>
<div class="container">
  <Hero />
  <LargeCardDisplay
    v-for="cardInfo in largeCardInfo"
    :key="cardInfo.id"
    :cardsSection="cardInfo"
  />
  <SmallCardDisplay 
    v-for="cardInfo in smallCardSections"
    :key="cardInfo.id"
    :cardsSection="cardInfo"
  />
</div>

</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";

export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      // smallCardSections: smallCardSections - This is equal to below because it is using the same name
      smallCardSections
    }
  }
}
</script>


<style scoped>

</style>
