<script setup>
import { GoogleMap, Marker } from 'vue3-google-map'

const center = { lat: 40.689247, lng: -74.044502 }
let apiKey = ''
// first commit
apiKey = 'second commit'
apiKey = 'third commit'
apiKey = 'fourth commit'
apiKey = 'fifth commit'

</script>

<template>
  <GoogleMap
    :api-key="apiKey"
    style="width: 100%; height: 500px;"
    :center="center"
    :zoom="15"
  >
    <Marker :options="{ position: center }" />
  </GoogleMap>
</template>

// helo helo
