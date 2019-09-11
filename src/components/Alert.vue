<template>
    <div :class="classname" @click="changeAlertClassName">
       {{help}} {{message}}
    </div>
</template>
<script>
export default {
    name: "Alert",
    props: ['message'],
    data: function(){
        return{
            help: "Help! I need somebody!",
            classname: "alert alert-success"
        }
    },
    methods:{
       changeAlertClassName: function(){
           if(this.classname === "alert alert-primary"){
               this.classname = "alert alert-success"
           }else{
               this.classname = "alert alert-primary"
           }
          }
    }
}
</script>

<style lang="scss">
   .alert{
        position: relative;
        padding: .75rem 1.25rem;
        margin-bottom: 1rem;
        border: 1px solid transparent;
        border-radius: .25rem;
        cursor: pointer;
   }

    .alert-primary {
        color: #004085;
        background-color: #cce5ff;
        border-color: #b8daff;
    }

    .alert-success{
        color: #721c24;
        background-color: #f8d7da;
        border-color: #f5c6cb;
    }
</style>