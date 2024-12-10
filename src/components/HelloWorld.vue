<template>
  <div>
    <h1>Login form</h1>
    <div
      :style="{
        display: 'flex',
        flexDirection: 'column',
        width: '100%',

        alignItems: 'center',
        justifyContent: 'center',
      }"
    >
      <input
        type="text"
        v-model="LoginForm.name"
        placeholder="Enter your name"
      /><br />

      <input
        type="password"
        v-model="LoginForm.password"
        placeholder="Enter your password"
      /><br />

      <button @click="getLogin">Login</button>
    </div>
  </div>
<div>  <h1>{{lastName}}</h1></div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      LoginForm: {
        name: null,
        password: null,
      },
      lastName: "jasjs",
    };
  },
  beforeCreate() {
    this.lastName="Sree"
    console.log("beforectrae",this.lastName)
  },
  created() {
    //  this.lastName="Sree"
    console.log("created",this.lastName)
  },
  methods: {
    getLogin() {
      console.log("login info", this.LoginForm);
    },
  },
};
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
