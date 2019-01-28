<template>
  <div>
    <keep-alive>
      <component v-bind:is="component"></component>
    </keep-alive>
   <button v-on:click="component='form-one'">Show form one</button>
   <button v-on:click="component='form-two'">Show form Two</button>
  </div>
</template>

<script>


import FormOne from './components/FormOne.vue'
import FormTwo from './components/FormTwo.vue'

export default {

  data(){

    return{
      component: 'form-two'
    }
  },
  components: {

    'form-one': FormOne,
    'form-two': FormTwo
  }
}
</script>

<style scoped>

</style>
