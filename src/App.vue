<template>
  <div class="h-100 d-flex flex-column">
    <h1 class="flex-grow-0">
      Vue with OSD
    </h1>
    <div class="osd-container d-flex flex-row flex-grow-1 ">
      <div class="flex-grow-1 bg-secondary" id="osd-container-1"></div>
      <div class="flex-grow-1 bg-primary" ref="osd-container-2"></div>
    </div>
    
  </div>
</template>
<script>
export default {
  mounted() {

    // creaing OSD by id
    OpenSeadragon({
      id:              "osd-container-1",
      prefixUrl:       "https://openseadragon.github.io/openseadragon/images/",
      tileSources:     "https://openseadragon.github.io/example-images/duomo/duomo.dzi"
    })

    // creating OSD instance using $ref
    OpenSeadragon({
      element:         this.$refs['osd-container-2'],
      prefixUrl:       "https://openseadragon.github.io/openseadragon/images/",
      tileSources:     "https://openseadragon.github.io/example-images/duomo/duomo.dzi"
    })
  }
}
</script>
