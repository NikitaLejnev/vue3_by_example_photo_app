<template>
  <div>
    <h1>Photos</h1>
    <button @click="load">Refresh</button>
    <div class="row">
      <div>Name</div>
      <div>Photo</div>
      <div>Description</div>
      <div>Actions</div>
    </div>
  </div>
</template>
 <script>
 import axios from "axios";
 import { APIURL } from '../constant';

 export default {
   data() {
     return {
       photos: [],
     };
   },
   methods: {}
 }
 </script>
 
 <style scoped>
 
 </style>
