<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" :data="data" />
  </div>
</template>

<script lang="ts">
import {Component, Vue, Prop} from "vue-property-decorator"
import HelloWorld from "@/components/HelloWorld.vue" // @ is an alias to /src

@Component({
  components: {
    HelloWorld,
  },
})
export default class HomeView extends Vue {
  data: Array<Record<string, any>> = [
    {
      id: 1,
      title: "VueJS",
    },
    {
      id: 2,
      title: "AngularJS",
    },
  ]
}
</script>
