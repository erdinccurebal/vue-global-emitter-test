<template>
  <div>
    <h1>Hello World Component</h1>
    <input v-model="globalData" type="text">
    <button @click="globalEmit">TEST</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      globalData: ''
    }
  },
  methods: {
    globalEmit(){
      this.emitter.emit("globalSend", this.globalData)
    }
  }
}
</script>

<style>

</style>