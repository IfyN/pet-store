<template>
  <v-container grid-list-md fluid>
    <v-layout wrap>
      <v-flex xs12 sm4 md3 v-for="pet in dogs" :key="pet.breed">
        <v-card color="grey lighten-2">
          <!--v-img src="https://goo.gl/6CQNDo" height="170px"> </v-img!--->
          <!---replace with!--->
          <v-img :src="pet.img" height="170px"></v-img>

          <v-card-title>
            <div>
              <!--h3>Looking for a dog?</h3-->
              <!--replace with-->
              <h3>{{ pet.name }}</h3>
              <p>{{ pet.breed }}</p>
            </div>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import { Dogs } from "../data/dogs";
export default {
  data() {
    return {
      dogs: Dogs,
    };
  },
};
</script>



<style scoped>
p {
  margin: 0;
}
</style>
