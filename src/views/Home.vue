<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import _ from "lodash";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
  data() {
    return {
      temp1: {
        name: "zhangsan",
        children: [
          {
            age: 20,
          },
        ],
      },
      temp2: {
        name: "zhangsan",
        children: [
          {
            age: 20,
            children: [
              {
                sex: 1,
              },
            ],
          },
        ],
      },
    };
  },
  methods: {
    fn() {
      console.log(_.isEqual(this.temp1, this.temp2));
    },
  },
  created() {
    this.fn();
  },
};
</script>
