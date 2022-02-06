<template>
  <div class="q-pa-md">
    <div class="row">
      <div class="col"  v-for="(row, index) in rows.slice(0,6)" :key="row.name">
        <q-card class="my-card">
          <q-img
            :src="row.name"
            :style='rows[index].style' @click="rows[index].style = rows[index].style ? '' : 'filter: grayscale(100%)'"
          />
        </q-card>
      </div>
    </div>
    <div class="row">
      <div class="col"  v-for="(row, index) in rows.slice(6,12)" :key="row.name">
        <q-card class="my-card">
          <q-img
            :src="row.name"
            :style='rows[index + 6].style' @click="rows[index + 6].style = rows[index + 6].style ? '' : 'filter: grayscale(100%)'"
          />
        </q-card>
      </div>
    </div>
    <div class="row">
      <div class="col"  v-for="(row, index) in rows.slice(12,18)" :key="row.name">
        <q-card class="my-card">
          <q-img
            :src="row.name"
            :style='rows[index + 12].style' @click="rows[index + 12].style = rows[index + 12].style ? '' : 'filter: grayscale(100%)'"
          />
        </q-card>
      </div>
    </div>
    <div class="row">
      <div class="col"  v-for="(row, index) in rows.slice(18,24)" :key="row.name">
        <q-card class="my-card">
          <q-img
            :src="row.name"
            :style='rows[index + 18].style' @click="rows[index + 18].style = rows[index + 18].style ? '' : 'filter: grayscale(100%)'"
          />
        </q-card>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

const columns = [
  {
    name: 'name',
    required: true,

    align: 'left',
    field: row => row.name,
    format: val => `${val}`,
    sortable: true
  }
]

const rows = [{
  name: 'icons/earthorb.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/waterjewel.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/windjade.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/fireruby.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/eletalebook.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/darkgaolkey.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/solvaring.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/zelse.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/nepty.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/shilf.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/fargo.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/guilty.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/yellowwings.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/bluewings.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/greenwings.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/redwings.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/ivorywings.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/blackwings.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/fire.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/water.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/earth.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/wind.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/lavarr.png',
  style: 'filter: grayscale(100%)'
}, {
  name: 'icons/beigis.png',
  style: 'filter: grayscale(100%)'
}]

export default {

  setup () {
    return {
      columns,
      rows: ref(rows)
    }
  }
}
</script>

<style>
.my-card {
  margin: 2px;
  /* max-width: 128px;
  max-width: 128px; */

}
</style>
