<template>
  <div class="container">
    <h2>Add a New User</h2>
    <div class="input-group">
      <input placeholder="username" type="text" v-model="username" />
    </div>
    <div class="input-group">
        <input placeholder="age" type="text" v-model="age" />
    </div>
    <button @click="addUser">Add User</button>
  </div>
</template>
<script>
export default {
  emits: ['add-user'],
  data() {
    return {
      username: "",
      age: ""
    }
  },
  methods: {
    addUser() {
      let username = this.username,
          age = this.age;
      
      this.$emit('add-user', username, age);
    }
  }
};
// UserData should output two input fields => for name and age
</script>
<style>
.container {
  width: 300px;
  border: 1px solid black;
  border-radius: 15px;
}
input {
  border:1px solid black;
  border-radius: 3px;
  margin:5px;
  width:180px;
  height:22px;
}
button {
  border:1px solid brown;
  border-radius: 3px;
  background-color: burlywood;
  padding:7px;
  margin-top:5px;
  color:black
}
button:hover {
  border:1px solid burlywood;
  background-color: brown;
  color: white;
}
</style>
