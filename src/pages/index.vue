<template>
  <v-layout class="rounded rounded-md border">
    <v-navigation-drawer v-model="drawer" color="surface-variant" permanent></v-navigation-drawer>
    <div class="">
      <li>Home</li>
      <li>Contact</li>
    </div>
    <v-app-bar
      :order="order"
      color="grey-lighten-2"
      title="Application bar"
      flat
    >
      <template v-slot:append>
        <v-switch
          v-model="order"
          class="me-2"
          false-value="0"
          label="Toggle order"
          true-value="-1"
          hide-details
          inset
          base-color="red"
          center-affix="prependInner"
          color="primary"
          defaults-target="v-switch"
          error="true"
          error-messages="Error message"
          false-icon="mdi-close"
          true-icon="mdi-check"
        ></v-switch>
      </template>
    </v-app-bar>

    <v-main class="d-flex align-center justify-center" height="100vh">
      <v-container>
        <v-sheet
          border="dashed md"
          color="surface-light"
          height="100"  
          rounded="lg"
          width="100%"
        ></v-sheet>
      </v-container>
    </v-main>
  </v-layout>
</template>

<script setup>
import { onMounted, ref, watch } from 'vue'

const order = ref(0)
const drawer = ref(false)


watch(order, (newValue) => {
  console.log('Order changed to:', newValue)
})

onMounted(() => {
  setTimeout(()=>{
    drawer.value = true
  }, 3000) // Any initialization logic can go here
})


</script>