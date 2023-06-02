<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function () {
    return {
      msg: null
    }
  },
  mounted: function name() {
    const vm = this
    fetch('http://localhost:8000/api')
    .then(res => res.json())
    .then(res => {
      vm.msg = res.msg
    })
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
