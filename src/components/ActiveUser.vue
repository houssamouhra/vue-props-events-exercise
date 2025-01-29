<template>
  <section>
    <h2>{{ username }}</h2>
    <h3>{{ userage }} Years Old</h3>
  </section>
</template>

<script>
export default {
  props: {
    username: {
      type: String,
      required: true,
    },
    userage: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>

<style>
html {
  font-family: Arial, Helvetica, sans-serif;
}

section {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid #ccc;
  background-color: rgb(180, 210, 227);
  text-align: center;
}

input {
  padding: 10px;
  margin: 5px;
}

button {
  background-color: rgb(16, 60, 98);
  padding: 10px;
  margin: 10px;
  border: none;
  border-radius: 8px;
  color: white;
  text-decoration: none;
}

button:hover {
  background-color: rgb(22, 82, 133);
}
</style>
