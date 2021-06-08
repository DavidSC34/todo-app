<template>
        <v-text-field
            class="pa-3"
           v-model="newTaskTitle"
           @click:append="addTask"
           @keyup.enter="addTask"
            outlined
            label="Add Task"
            append-icon="mdi-plus"
            hide-details
            clearable
          ></v-text-field>
</template>

<script>
export default {
 data(){
      return{
        newTaskTitle:'',
       
      }
    },
    methods: {
      addTask(){
          
        this.$store.commit('addTask',this.newTaskTitle);
        this.newTaskTitle = '';
      }   
        
    }
}
</script>

<style>

</style>