<template>
  <button @click="handler">
    거울을 바라본다.
  </button>
  <h1 v-if="isShow">
    내가 보이고 있지 ? 
  </h1>  
  <h1 v-else-if="count > 3 ">
    거울을 바라보는 건 누구였을까?
  </h1>
  <h1 v-else>
    보이지 않는 척을 하는 구나.
  </h1>
</template>

<script>
export default {
  data(){
    return{
      isShow : true,
      count : 0
    }
  },
  methods:{
    handler(){
      this.isShow = !this.isShow; 
      this.count+=1;
    }
  }
}
</script>
