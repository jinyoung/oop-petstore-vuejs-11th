<template>

  <Pet v-model="value"></Pet>
 
</template>

<script>

  import Pet from './Pet'

  export default {
    name: 'Dog',

    components:{
      Pet
    },

    mixins: [Pet],


    methods:{

      eat(){
        this.value.energy += 2; //this.energy = this.energy + 2;
      },

      sleep(){
        //this.energy++;
        this.$super(Pet).sleep();
      
        this.value.appearance ++;
      }


    }
  }
</script>
