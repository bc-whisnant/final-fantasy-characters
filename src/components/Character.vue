<template>
    <b-col class="character-container" cols="4">
      <b-card>
        <img class="ff-image" :src="picture" alt>
        <h3>{{ name }}</h3>
        <h4>{{ origin }}</h4>
        <h4>{{ job }}</h4>
        <h4>{{ gender }}</h4>
        <h4>{{ age }}</h4>
      </b-card>
    </b-col>
</template>

<script>
export default {
  name: "Character",
  props: {
    name: String,
    origin: String,
    job: String,
    gender: String,
    age: String,
    picture: String
  }
};
</script>

<style scoped>
.character-container {
  margin-bottom: 2%;
  text-align: center;
}
.ff-image {
  width: 200px;
  height: 300px;
}
</style>
