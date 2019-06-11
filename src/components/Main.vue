<template>
  <div>
    <h1>List of users :</h1>
    <ul>
      <li class="user-item" v-for="user in getUsersNames" :key="user.id">
        <span>name: {{user.name}}</span>
        <span>name: {{user.age}}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["getUsers"],
  data() {
    return {};
  },
  components: {},
  computed: {
    getUsersNames() {
      return this.getUsers;
    }
  },
  mounted() {
    console.log(this.getUsersNames);
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.user-item {
  display: flex;
  flex-direction: column;
  & span {
    cursor: pointer;
    margin: 0.5rem 0;
    border-bottom: 1px solid grey;
    border-left: 5px solid silver;
    max-width: 100px;
    padding: 0.5rem;
    box-shadow: 0 0 5px rgba(128, 128, 128, 0.384);
  }
  & span:hover {
    background: rgba(223, 223, 223, 0.63);
  }
}
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
