<script setup>
import { ref } from "vue"

const tasks = ref([
    {
    name: 'Task 1',
    time: 30
}, {
    name: 'Task 2',
    time: 40
}, {
    name: 'Task 3',
    time: 60
}, {
    name: 'Task 4',
    time: 45
}, {
    name: 'Task 5',
    time: 50
}]);

function addNewTask(){
    const newTask = {
        id: tasks.value.length+1,
         name: `Task Name ${tasks.value.length+1}`,
            time: `Time ${tasks.value.length+30
        }`
    };
    tasks.value.push(newTask);
}
function delateNewTask(){
    const newTask = {
        id: tasks.value.length+1,
        name: `Task ${tasks.value.length+1}`
    };
    tasks.value.pop(newTask);
}
function editNewTask(){
    alert("update your task?")
}
</script>
  <template>
<ul v-for = "task in tasks"  :key = " task.id " >
    <li> {{ task.name }}  {{ task.time }} </li>
    <li></li>
</ul>
<button @click="delateNewTask ()"> Delete new task</button>
<br>        
<button @click=" addNewTask ()"> Add new task</button>
<button @click=" editNewTask ()"> edit</button>
        



  </template>
  <style scoped>
</style>