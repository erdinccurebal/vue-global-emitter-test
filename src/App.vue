<template>
  <HelloWorld />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  components: {
    HelloWorld
  },created(){
    this.emitter.on("globalSend", eventData => {
      console.log(eventData)
    });
  }
}
</script>
