<template>

    <Pet v-model="value">

      <template v-slot:buttons>
        <v-btn  outlined
        rounded
        text @click="groom">GROOM</v-btn>
      </template>

    </Pet>

</template>

<script>

  import Pet from './Pet'

  export default {
    name: 'Cat',

    mixins: [Pet],

    components:{
      Pet
    },

    
    methods:{

      groom(){
        this.value.appearance ++;
      }


    }
  }
</script>
