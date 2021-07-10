This would be the base products page
<template>
<div></div>
  <div class="container">
    <LargeCardDisplay
      v-for="cardInfo in largeCardSections.slice(0,1)"
      :key="cardInfo.id"
      :cardSection="CardInfo"
    />
    <SmallCardDisplay
      v-for="cardInfo in smallCardSections.slice(0,1)"
      :key="cardInfo.id"
      :cardSection="CardInfo"
    />
  </div>
</template>

<script>
import {largeCardSections, smallCardSections} from "@/assets/data/js"

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