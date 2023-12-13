<script>

export default{
  data(){
    return{
      menuSideValue: 0,
    }
  },
  methods: {
      changeMenu(){
         if(this.menuSideValue){
          this.menuSideValue = 0
         }else{
          this.menuSideValue  = 1
         }
         console.log(this.menuSideValue)
      }
    },
  
}
</script>

<template>
  <header>
    <div  @click="changeMenu"  :class="this.menuSideValue ? 'burger-on': 'burger-off' "  >
      <div class="divmenu">
        <div class="l1"></div>
        <div class="l1"></div>
        <div class="l1"></div>
      </div>
    </div>

    <div class="nav-on" :class="this.menuSideValue ? 'nav-on': 'nav-off'">

    </div>
    
  </header>
</template>

<style scoped lang="scss">

header{
  display: flex;
  justify-content: flex-end;
  .divmenu{
    display: flex;
    flex-direction: column;
    gap:5px;
    .l1{
      width:30px;
      height: 5px;
      background-color: black;
    }
  }

}


.nav-on{
 width: 100vw;
 height: 100vh;
 position: fixed;
 top:0px;
 right:0px;
 background-color:red;
 transition: all .4s linear;
}
.nav-off{
width: 0;
  
}

.burger-on{
  position: fixed;
  z-index: 1 ;
}
.burger-off{
  position: fixed;
  z-index: 1 ;
}


</style>
