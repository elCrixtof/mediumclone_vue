<template>
  <div>
    <!-- <h1>Medium Clone</h1> -->
    <ThisIsExample/>
    <router-view></router-view>
  </div>
</template>

<script>
import ThisIsExample from '@/components/ThisIsExample.vue';
  export default {
  name: 'HomeView',
  components: {
    ThisIsExample
  }
}
</script>
