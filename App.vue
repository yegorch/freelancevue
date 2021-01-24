<template>
  <the-navbar></the-navbar>
  <div class="container with-nav">
    <router-view></router-view>
  </div>
</template>

<script>
import TheNavbar from './components/TheNavbar'
import Tasks from './views/Tasks'
import {useStore} from 'vuex'

export default {
  setup() {
        const store = useStore()
        store.commit('initStore')
    },
  components: { TheNavbar,Tasks }
}
</script>

<style>

</style>
