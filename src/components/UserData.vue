<template>
  <section>
    <form @submit.prevent="submitData">
      <input
        id="name"
        type="text"
        placeholder="Your name"
        v-model="enteredName"
      />
      <input id="age" type="text" placeholder="Your age" v-model="enteredAge" />
      <button>Set Use Data</button>
    </form>
  </section>
</template>

<script>
export default {
  emits: ["submit-data"],
  data() {
    return {
      enteredName: "",
      enteredAge: "",
    };
  },
  methods: {
    submitData() {
      this.$emit("submit-data", this.enteredName, this.enteredAge);
    },
  },
};
</script>
