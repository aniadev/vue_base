<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ul class="data">
      <li
        class="data-item"
        v-for="item in data"
        :key="item.id"
      >
        {{ item.title }}
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import {Component, Prop, Vue} from "vue-property-decorator"

@Component
export default class HelloWorld extends Vue {
  @Prop() public msg!: string
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
