<template>
  <div>
    <h1>App vue file</h1>
    <Main :getUsers="getUsers"/>
  </div>
</template>


<script>
import Main from "./components/Main";
export default {
  data() {
    return {
      nameList: [{ name: "John", age: 20 }, { name: "Jannet", age: 26 }]
    };
  },
  components: { Main },
  computed: {
    getUsers() {
      return this.nameList;
    }
  },
  methods: {},
  mounted() {}
};
</script>
