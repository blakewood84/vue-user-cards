<template>
  <div class="center">
    <user-data @add-user="addNewUser"></user-data>
    <active-user
      v-for="user in users"
      :key="user.id"
      :username="user.username"
      :age="user.age"
    ></active-user>
  </div>
</template>
<script>
import ActiveUser from "./components/ActiveUser.vue";
import UserData from './components/UserData.vue';
export default {
  components: { ActiveUser, UserData },
  data() {
    return {
      users: [
        {
          id: 0,
          username: "HelloKitty",
          age: "32",
        },
        {
          id: 1,
          username: "HappyLow",
          age: "29",
        },
      ],
    };
  },
  methods: {
      addNewUser(username, age) {
          let newUser = {
              id: new Date().toISOString(),
              username: username,
              age: age
          };
          this.users.push(newUser);
      }
  }
};
</script>
<style>
.center {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
</style>
