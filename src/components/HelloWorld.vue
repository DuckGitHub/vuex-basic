<template>
  <div class="container">
    <h3>Counter: {{ $store.state.count }} times, counter is {{ evenOrOdd }}</h3>
    <button class="btn btn-success" @click="increment">+</button>
    <button class="btn btn-danger" @click="decrement">-</button>
    <button class="btn btn-warning" @click="incrementIfOdd">Increment if Odd</button>
    <button class="btn btn-primary" @click="incrementAsync">Increment Async</button>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'

export default {
  name: 'HelloWorld',
  computed: mapGetters([
    'evenOrOdd'
  ]),
  methods: mapActions([
    'increment',
    'decrement',
    'incrementIfOdd',
    'incrementAsync'
  ])
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
