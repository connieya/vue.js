<template>
  <!-- form의 기본 동작은 새로고침이다.  -->
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username"> id: </label>
      <input type="text" id="username" v-model="username">
    </div>
    <div>
      <label for="password">pw:</label>
      <input type="text" id="password" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
export default {
  data : function(){
    return{
      username: '',
      password: '',

    }
    
  },
  methods: {
      submitForm : function(){
        // event.preventDefault(); 일반 자바스크립트 , 제이쿼리에서 사용함 
        console.log(this.username, this.password);

      }
    }

}
</script>

<style>

</style>