<script>
export default {
  data() {
    return {
      msg: 0
      
    }
  },

  methods: {
    increment() {
      this.msg = this.msg + 1 
    },
    
    decrement() {
      if (this.msg > 0) {
        this.msg = this.msg - 1 
      }
    },

    reset() {
      this.msg = 0
    }
  }
}
</script>

<template>
  <h1>{{ msg }}</h1>
  <button @click="increment">Increment</button>

  <button @click="decrement">Decrement</button>
  <br><br>
  <button @click="reset">Reset</button>
</template>