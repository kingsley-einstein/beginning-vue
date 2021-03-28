<template>
 <div class="tasks"></div>
 <div v-for="t in tasks" v-bind:key="t.id">
  <div>{{t.title}}</div>
 </div>
</template>
<script>
 export default {
  name: "Tasks",
  data: () => ({
   tasks: [{
    title: "Play Football",
    id: 1,
    done: false
   }]
  }),
  methods: {
   addTask(task) {
    this.tasks = this.tasks.concat(task);
   }
  },
  created() {
   console.log("Component is created");
  }
 }
</script>