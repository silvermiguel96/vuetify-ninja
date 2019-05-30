<template>
  <div class="Dashboard">
    <h1 class="subheading grey--text">Dashboard</h1>
    <v-container class="my-5">
      <v-card flat v-for="project in projects" :key="project.title">
        <v-layout row wrap :class="`pa-3 project ${project.status}`">
          <v-flex xs12 md6>
            <div class="caption grey--text">Project title</div>
            <div>{{ project.title }}</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Person</div>
            <div>{{ project.person }}</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Due By</div>
            <div>{{ project.due }}</div>
          </v-flex>
          <v-flex xs2 sm4 md2>
            <div class="caption grey--text">Status</div>
            <div>{{ project.status }}</div>
          </v-flex>
        </v-layout>
        <v-divider></v-divider>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        { title: 'Design a new Website', person: 'The Net Ninja', due: '1st Jan 2019' ,status: 'completed'},
        { title: 'Design a new Website', person: 'The Net Ninja', due: '1st Jan 2019' ,status: 'ongoing'},
        { title: 'Design a new Website', person: 'The Net Ninja', due: '1st Jan 2019' ,status: 'overdue'},
        { title: 'Design a new Website', person: 'The Net Ninja', due: '1st Jan 2019' ,status: 'ongoing'}
      ]
    }
  }
};
</script>
<style>
.project.completed {
  border-left: 4px solid #3cd1c2;
}
.project.ongoing {
  border-left: 4px solid orange;
}
.project.overdue {
  border-left: 4px solid tomato
  ;
}
</style>
