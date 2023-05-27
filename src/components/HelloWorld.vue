<template>
 <v-container>
  <v-row class="mt-8">
    <!-- empty column -->
    <v-col cols="3">      
    </v-col>
    <!-- main column -->
    <v-col cols="6">
      <div class="d-flex">
      <v-text-field class="headline" v-model="name"></v-text-field>
      <v-btn class="mt-3 green white--text" @click="getData">Add me</v-btn>
      <v-btn class="mt-3 ms-2 red white--text" @click="deleteData">delete me</v-btn>
      </div>     
    </v-col>
    <!-- empty column -->
    <v-col cols="3">
    </v-col>
  </v-row>
 {{ name }}
  <!-- table space -->
  <v-data-table
  :headers = "headers"
  :items = "deserts"
  v-if="addingData=deserts.length>0"
  item-key="name"
  show-select
  single-select
  class="elevation-1 display-title"

  >

  </v-data-table>

  
 </v-container>
 
</template>
<script>
export default{
  name:'HelloWorld',

  data(){
    return{
      name:'',
      fetcheData:[],
      seen:false,
      addingData:false,
      deserts:[
        
      ],
      headers:[
        {text:'Task Name', align:'start', value:'name'},
        // {text:'Category', value:'category'}
      ]
    }
  },
  methods:{
    getData(){
      this.deserts.push({name:this.name})
      this.name=''
     
    },
    deleteData(){
      for(let d = 0; d < this.deserts.length; d++){
    
    let txt = ''

       txt = this.deserts[d]
      if(txt === this.name){
       this.deserts.splice(txt,0)
      }
     
      console.log(txt);
      
   }
    }
   
  }
 
}
</script>