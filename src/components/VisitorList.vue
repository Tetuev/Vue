<template>
    <div>
             <h1>List of Hospital Visitors</h1>
         <button @click="getVisitors">Load Visitors</button>
         <div v-for="visitor in visitors" :key="visitor.id">
             <h3>{{visitor.id}}. {{visitor.name}}</h3>
             <p>phone: {{visitor.mobile}}</p>
             <p>date/time: {{visitor.date}}</p>
             <p>status: {{visitor.status}}</p>
             <p>access: {{visitor.access}}</p>
             <hr />
         </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
     name: 'VisitorList',
     data() {
         return{
             visitors: [],
         }
     },
     methods:{
         getVisitors(){
              axios.get('http://localhost:3000/visitors')
              .then((response) => {
                   console.log(response.data)
                   this.visitors = response.data
              })
              .catch((error) => {
                  console.log(error)
              })
         }
     }
}
</script>

<style scoped>

</style>