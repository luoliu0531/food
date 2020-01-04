<template>
  <div>
    <map
     id="map"
     scale="14" 
     :markers="markers" 
     show-location 
     style="width: 100%; height: 600px;"
     >
     </map>
  </div>
</template>

<script>
export default {
  data () {
    return {
      
    markers: [{
      id: 0,
      latitude: 23.099994,
      longitude: 113.324520,
      width: 50,
      height: 50
    }],
    }
  },

  methods: {
  },

  created () {
  }
}
</script>

<style scoped>
</style>
