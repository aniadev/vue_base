<template>
  <div class="hello">
    <h1>Hello World</h1>
    <div v-for="item in data" :key="item.id">
      <li>title: {{ item.title }}</li>
    </div>
  </div>
</template>

<script lang="ts">
import {Component, Prop, Vue} from "vue-property-decorator"

@Component
export default class HelloWorld extends Vue {
  @Prop() public data!: Array<Record<string, any>>
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
