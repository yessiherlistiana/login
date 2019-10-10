<template>
  <q-page class="flex flex-center">
    
    <input v-model = "message"   @keyup = "handleKeyup"/>
    <button @click ="clearMessage">clear</button>
 <H5> {{message}} </H5>
  </q-page>
</template>

<script>
export default {
 
data(){
  return{
  message: 'Test Vue'
}
},

//menghapus menggunakan method
methods:{
  clearMessage(){
    this.message=''
  },

//menggunakan kode ASCII
handleKeyup(e){
  if (e.keyCode == 27){
    this.message = 'ESC'
  }
  else if (e.keyCode == 13){
    this.message = 'ENTER'
  }
}
}
}
</script>
