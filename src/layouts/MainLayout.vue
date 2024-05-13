<template>
  <q-layout view="hHh Lpr lFf">
    <q-header style="background-color: #1b2727;">
      <q-toolbar class="text-center">
        <q-toolbar-title>
          Daily Word App
        </q-toolbar-title>
        <!--<q-icon name="roundFormatQuote"></q-icon>-->
        <!-- <q-toggle v-model="$q.dark.isActive">
          {{ $q.dark.isActive ? 'active' : 'disabled' }}
        </q-toggle> -->
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import { useQuasar } from 'quasar'
import { watch } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  setup () {
    const leftDrawerOpen = ref(false)
    const $q = useQuasar()

    watch(() => $q.dark.isActive, val => {
      console.log(val ? 'On dark mode' : 'On light mode')
    })

    // get status
    console.log($q.dark.isActive) // true, false

    // get configured status
    console.log($q.dark.mode) // "auto", true, false

    return {
      darkMode () {
        $q.dark.isActive = !$q.dark.isActive
      },
    }
  }
})
</script>

<style>
.btn-color {
  background: rgb(27,39,39);
  background: linear-gradient(0deg, rgba(27,39,39,1) 0%, rgba(60,81,72,1) 100%);
}
</style>
