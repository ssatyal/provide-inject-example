<template>
  <div class="hello">
    <nest-one/>
    <button @click="changeMessage">change message</button>
  </div>
</template>

<script>
import NestOne from './nest-one.vue';
export default {
  name: 'HelloWorld',
  components: {
    NestOne,
  },
  props: {
    msg: String
  },
  provide() {
    return {msg: this.msg}
  },
  methods: {
    changeMessage() {
      this.msg = `${this.msg} clicked`
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
