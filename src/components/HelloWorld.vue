<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <span>The one with error:</span>
    <vs-slider
            :min="0.8"
            :max="1.3"
            ticks
            :step="0.1"
            :step-decimals="true"
            v-model="val"
    />
    <br>
    <span>However, this one works correctly as long as you don't use bind on max prop:</span>
    <vs-slider
            :min="0.8"
            max="1.3"
            ticks
            :step="0.1"
            :step-decimals="true"
            v-model="val"
    />
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      val: 1.0
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
