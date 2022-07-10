<template>
  <div class="container text-center mt-5">
    <div class="mt-5"><label for="">選擇身分</label> <input type="text" /></div>

    <br />
    <div class="mt-5"><label for="">帳號</label> <input type="name" /></div>
    <br />
    <div class="mt-5"><label for="">密碼</label> <input type="password" /></div>
    <br />
    <router-link to="/home"
      ><div class="btn btn-primary text-light">Login</div></router-link
    >
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
body {
  background-color: #35628d;
}
</style>
