<template>
  <b-container>
    <b-row class="ml-auto mr-auto text-center">
      <h3>Final Fantasy Characters</h3>
    </b-row>
    <b-row>
      <Character
        v-for="character in characters"
        :key="character.id"
        :img="character.picture"
        :name="character.name"
        :origin="character.origin"
        :job="character.job"
        :gender="character.gender"
        :age="character.age"
        :picture="character.picture"
      />
    </b-row>
  </b-container>
</template>

<script>
import Character from "./Character.vue";
import axios from "axios";
export default {
  name: "CharacterContainer",
  components: {
    Character
  },
  data() {
    return {
      characters: []
    };
  },
  mounted() {
    this.getCharacters();
  },
  methods: {
    getCharacters() {
      axios
        .get("https://www.moogleapi.com/api/v1/characters")
        .then(response => {
          this.characters = response.data;
          console.log(this.characters);
        });
    }
  }
};
</script>
