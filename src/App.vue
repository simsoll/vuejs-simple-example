<template>
  <div>
    <p>Parent Vue instance: {{ total }}</p>
    <button-counter v-bind:start="0" v-on:increment="incrementTotal"></button-counter>
    <button-counter v-bind:start="1" v-on:increment="incrementTotal"></button-counter>
  </div>
</template>

<script>
import ButtonCounter from './ButtonCounter.vue'

export default {
  components: {
    buttonCounter: ButtonCounter
  },
  data: function() {
    return {
      total: 0
    }
  },
  methods: {
    incrementTotal: function() {
      this.total += 1
    }
  }
}
</script>

<style lang="scss">

</style>
