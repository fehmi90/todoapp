<template>
  <div class="container mt-5">
    <h1 class="mt-5">My vue to do App </h1>

    <div class="d-flex">

      <input v-model="task" type="text" class="form-control mr-2">
      <button @click="submitTask" class="btn btn-warning">submit</button>
    </div>

<div class="container mt-5">

<table class="table">
  <thead class="thead-dark">
    <tr>
      <th scope="col">Task</th>
      <th scope="col">Status</th>
      <th scope="col">#</th>
      <th scope="col">#</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="(task, index) in tasks" :key="index">
      <th scope="row">{{task.name}}</th>
    
      <td>{{task.status}}</td>
      <td><div @click="editTask(index)"><span class="fa fa-pen"></span></div></td>
      <td><div @click="deleteTask()"><span class="fa fa-trash"></span></div></td>
    </tr>

  
  </tbody>
</table>


</div>
      

</div>
</template>

<script>
export default {
  name:"todoApp",

  data(){
    return{
        task: '',
        editedTask : null,

     tasks:[
       {
         name: 'line 1 du tabel',
       status: 'in progress'
       },

      {
        name: 'line 2 du tabel',
       status: 'done'
       }
]


    }

  },

   methods: {
    submitTask () {
       
      if (this.task.length === 0) return ;
     if (this.editedTask === null) {
      this.tasks.push({
         name: this.task,
         status: 'to-do'

      });
      } else{
        this.tasks[this.editedTask].name = this.task;

      }


    },



    deleteTask(index){
     this.tasks.splice(index,1)



    },

    editTask(index){

      this.task = this.tasks[index].name;
      this.editedTask = index;
      
     
    }

  }

};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
