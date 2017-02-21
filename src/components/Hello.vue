<template>
  <div class="hello">
    <div class="wrap">
      <h1>{{ msg }}</h1>
    </div>
    <div>
      <MonacoEditor
        height='200'
        language="typescript"
        :code='code'
      >
    </div>
  </div>
</template>

<script>
import MonacoEditor from 'vue-monaco-editor'

export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to MonacoEditor example',
      code: `var hello = 'world'\nconsole.log(hello)`
    }
  },
  components: {
    MonacoEditor
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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

.wrap {
  text-align: center;
}
</style>
