<!-- <template v-slot:item.actions="{ item }">
   <div>
    <v-icon
      small
      class="mr-2"
      @click="editItem(item)"
    >
      mdi-pencil
    </v-icon>
    <v-icon
      small
      @click="deleteItem(item)"
    >
      mdi-delete
    </v-icon>
   </div>
  </template>
<script>
export default{
    name:'FontAwesome',
   
    data(){
        return{
            desserts: [],
            editedItem: {
        name: '',
        calories: 0,
        fat: 0,
        carbs: 0,
        protein: 0,
      },
      editItem (item) {
        this.editedIndex = this.desserts.indexOf(item)
        this.editedItem = Object.assign({}, item)
        this.dialog = true
      },

      deleteItem (item) {
        this.editedIndex = this.desserts.indexOf(item)
        this.editedItem = Object.assign({}, item)
        this.dialogDelete = true
      },
        }
    }

}
</script> -->