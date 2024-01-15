<template>
  <div class="container">
      <h2 class="text-center mt-5">ToDo App</h2>
      <div class="d-flex mt-5">
        <input type="text" placeholder="Enter Task" class="w-100 form-control" v-model="task">
        <button class="ms-2 btn btn-warning" @click="submitTask">add</button>
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
            <tr v-for="(task,index) in tasks" :key="index">
              <th scope="row">{{task.name}}</th>
              <td>{{task.status}}</td>
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
  name: 'todoApp',
  props: {
    msg: String
  },
  data(){
    return{
      task:'',
      tasks : [
        {
          name : 'Study English',
          status : 'todo',

        },
        {
          name : 'Study Django',
          status : 'inprogress',
        },
        {
          name : 'Study Vue.js',
          status : 'todo',
          
        },
        {
          name : 'Study Python',
          status : 'finshed',
          
        }
      ]
    }

  },
  methods:{
    submitTask(){
      if (this.task==0) return;
      this.tasks.push({
        name: this.task ,
        status: 'todo'
      })
    },
  },
}
</script>


<style scoped>
/* Add your component-specific styles here */
</style>
