<template>
  <div class="container">
      <h2 class="text-center mt-5">ToDo App</h2>
      <div class="d-flex mt-5">
        <input type="text" placeholder="Enter Task" class="w-100 form-control">
        <button class="ms-2 btn btn-warning">add</button>
      </div>

      <table class="table mt-5 table-bordered">
          <thead>
            <tr>
              <th scope="col">Task</th>
              <th scope="col">Status</th>
              <th scope="col">Edit</th>
              <th scope="col">Delete</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">Study js</th>
              <td>todo</td>
              <td>
                <div>
                <span class="fa fa-pen"></span>
              </div>
            </td>
              <td> 
                 <div>
                  <span class="fa fa-trash"></span>
                </div>
            </td>
            </tr>
           
          </tbody>
      </table>




  </div> 
</template>

<script>
export default {
  name: 'todoApp'
}
</script>

<style scoped>
/* Add your component-specific styles here */
</style>
