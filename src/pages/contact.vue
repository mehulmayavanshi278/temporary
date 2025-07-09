<script setup>
import { GoogleMap, Marker } from 'vue3-google-map'

const center = { lat: 40.689247, lng: -74.044502 }
let apiKey = 'AIzaSyDglblqg6uz0TFXU0hHQ6mEVhBJ9FliDOg'
// first commit
apiKey = 'second commit'

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
