<template>
  <div class="container mt-5">
    <h1 class="mt-5">My vue to do App </h1>

    <div class="d-flex">

      <input type="text" class="form-control mr-2">
      <button class="btn btn-warning">submit</button>
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
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td><span class="fa fa-pen"></span></td>
      <td><span class="fa fa-trash"></span></td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td><span class="fa fa-pen"></span></td>
      <td><span class="fa fa-trash"></span></td>
    </tr>
  
  </tbody>
</table>







</div>
      



   
   
  </div>
</template>

<script>
export default {
  
}
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
