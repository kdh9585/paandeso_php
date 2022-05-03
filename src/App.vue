<template>
  <div class="container">

    <nav>
      <router-link :to="{name:'Home'}">Home</router-link> |
      <router-link :to="{name:'Create'}">Ceate</router-link> |
      <router-link :to="{name:'List'}">List</router-link> |
      <router-link :to="{name:'About'}">About</router-link>
    </nav>

    <router-view />
  </div>


</template>

<script>
  import {useToast} from '@/composables/toast.js'
  export default {
    setup() {
      const {
        toastMessage,
        toastShow,
        triggerToast
      } = useToast();

      return {
        toastMessage,
        toastShow,
        triggerToast
      }
    }
  }
  
</script>

<style>
  #app {}
</style>