<template>
  <div class="jobs">
    <header><h1>PESO Job Listing</h1></header>
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="element in cardObjects" v-bind:key="element.job_id">
          <v-card class="text-xs-center ma-3">
            <v-responsive class="pt-4">
              <v-img src='../assets/Peso job listing.png' alt='image here'></v-img>
            </v-responsive>
          <v-card-text>
            <div class="subheading">{{element.content}}</div>
            <v-break></v-break>
            <div class="grey--text">{{element.email}}</div>
          </v-card-text>
          <v-card-actions>
            <v-btn color="grey" block >
              <v-icon left color="red">mdi-watch</v-icon>
              <span>VIEW JOB</span>
            </v-btn>
          </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Jobs",
  data(){
    return{
      cardObjects:[
        {job_id:1 ,content:"Job 1", email:"email 1"},
        {job_id:2 ,content:"Job 2", email:"email 2"},
        {job_id:3 ,content:"Job 3", email:"email 3"},
        {job_id:4 ,content:"Job 4", email:"email 4"},
        {job_id:5 ,content:"Job 5", email:"email 5"},
        {job_id:6 ,content:"Job 6", email:"email 6"},
      ]
    }
  }
};
</script>

<style scoped>
.jobs {
  text-align: center;
  background-color: green;
  margin: 10px;
  border: solid 2px;
  height: auto;
}
header {
  background-color: white;
  margin: 10px;
}
.buttn{
  justify-content: center;
}


</style>