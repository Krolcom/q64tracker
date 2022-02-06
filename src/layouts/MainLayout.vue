<template>
  <q-layout view="lHh  ">
    <q-header elevated>

    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {

  },

  setup () {
    return {

    }
  }
})
</script>
