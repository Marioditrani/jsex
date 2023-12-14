<script>
export default {
    data(){
        return{
            arr:[],
            input:'',
            
        }
    },
    methods:{
        pushinput(){
            this.arr.push(this.input)
            this.input=''
        }
    }
}

</script>

<template>
 <div class="input">
  <h1>Lista spesa</h1> 
   <input type="text" v-model="input">
   <button @click="pushinput">invio</button>
   <ul>
    <li v-for="i in arr" :key="i">
    {{ i }}
    </li>
   </ul>
 </div>
</template>

<style scoped lang="scss">

</style>
