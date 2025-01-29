<template>
  <active-user :username="user.name" :userage="user.age"></active-user>
  <user-data @submit-data="submitUserData"></user-data>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: "John Wick",
        age: 42,
      },
    };
  },
  methods: {
    submitUserData(name, age) {
      if (name.trim() === "" || age.trim() === "") {
        return alert("Fill the input fields!");
      } else {
        this.user = {
          name: name.trim(),
          age: +age,
        };
      }
    },
  },
};
</script>

<style></style>
