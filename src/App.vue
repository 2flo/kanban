<template>
    <div id="app">
       <h1>Bonjour</h1>
       <Alert message="Hello, it's me"></Alert>
    </div>
</template>
<script>
import Alert from './components/Alert.vue'
export default {
    name: "app",
    components: {
        Alert
    }
}
</script>

<style lang="scss">
   $color: red;
   h1{
      background-color: $color;
      color: white;
      text-align: center;
   }
</style>