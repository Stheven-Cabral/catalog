This would be the base products page
<template>
  <div>
    <div class="container">
      <LargeCardDisplay
        v-for="cardInfo in largeCardSections.slice(0,1)"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections.slice(0,1)"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import {largeCardSections, smallCardSections} from "@/assets/data.js"

  export default {
    data() {
      return {
        largeCardSections,
        smallCardSections
      }
    }
  }
</script>

<style scoped>

</style>