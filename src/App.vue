<template>
  <div id="app">
    <p>{{ count }}</p>
    <p>
      <button @click="increment">+</button>
      <button @click="decrement">-</button>
    </p>
  </div>
</template>

<script>


export default {
    computed: {
      count(){
          return this.$store.state.count
      }
    },
    methods: {
        increment () {
            this.$store.commit('increment')
            console.log(this)
        },
        decrement () {
            this.$store.commit('decrement')
        }
    }
}
</script>

<style type="text/sass" lang="sass">
#app
  color: red
</style>
