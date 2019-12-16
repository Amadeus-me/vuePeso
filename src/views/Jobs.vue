<template>
  <v-card class="ma-2 pa-2">
    <v-card-title class="justify-center purple white--text" > <h1>PESO Job Listing</h1> </v-card-title>
    <v-container class="row mx-2">
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-text-field append-icon="mdi-magnify" label="Search" v-model="search" class="pa-3"></v-text-field>
    </v-container>

    <v-data-table
      headers-length="7"
      :headers="columns"
      :items="jobs"
      :search="search"  
      show-select
      class="elevation-1"
      item-key="job_id"
    ></v-data-table>

    <v-btn fab color="success" fixed right bottom v-on:click="add('add')">
      <v-icon large >mdi-plus</v-icon>
    </v-btn>

    <v-container class="row">
      <v-btn v-on:click="add('save')" color="blue" class="ma-2">
        Save
        <v-icon>mdi-content-save-outline</v-icon>
      </v-btn>

      <v-btn v-on:click="add('edit')" color="neutral" class="ma-2">
        Edit
        <v-icon>mdi-pencil-outline</v-icon>
      </v-btn>

      <v-btn v-on:click="add('delete')" color="red" class="ma-2">
        Delete
        <v-icon>mdi-delete-outline</v-icon>
      </v-btn>
    </v-container>
  </v-card>
</template>

<script>
export default {
  name:"Jobs",
  data() {
    return {
      search: "",
      selected: [],
      columns: [
        { text: "Job ID", value: "job_id", align: "left", sortable: false },
        { text: "Company Name", value: "company_name" },
        { text: "Company Email", value: "company_email" },
        { text: "Hiring Details", value: "hiring_details" },
        { text: "Applied", value: "is_applied" },
        { text: "Saved", value: "is_saved" },
         { text: "Action", value: "action" }
      ],
      jobs: [
        {
          job_id: 1,
          company_name: "adidas",
          company_email: "nike@gmail.com",
          hiring_details: "hiring new sales representative",
          is_applied: 0,
          is_saved: 0,
        },
        {
          job_id: 2,
          company_name: "Nike",
          company_email: "nike@gmail.com",
          hiring_details: "hiring new sales representative",
          is_applied: 0,
          is_saved: 0
        },
        {
          job_id: 3,
          company_name: "Nike",
          company_email: "worldbalance@gmail.com",
          hiring_details: "hiring new sales representative",
          is_applied: 0,
          is_saved: 0
        },
        {
          job_id: 4,
          company_name: "Nike",
          company_email: "nike@gmail.com",
          hiring_details: "hiring new engineer",
          is_applied: 0,
          is_saved: 0
        },
        {
          job_id: 5,
          company_name: "Nike",
          company_email: "nike@gmail.com",
          hiring_details: "hiring new sales representative",
          is_applied: 0,
          is_saved: 0
        },
        {
          job_id: 6,
          company_name: "Nike",
          company_email: "nike@gmail.com",
          hiring_details: "hiring new sales representative",
          is_applied: 0,
          is_saved: 0
        },
        {
          job_id: 7,
          company_name: "Nike",
          company_email: "nike@gmail.com",
          hiring_details: "hiring new sales representative",
          is_applied: 0,
          is_saved: 0
        }
      ],
    };
  },
  methods:{
    add:function(message){
      alert(message)
    }
  }
};
</script>