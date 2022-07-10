<script setup>
import NavbarSidebar from "../components/NavbarSidebar.vue";
import { ref, onMounted } from "vue";

const date = ref();

// For demo purposes assign range from the current date
onMounted(() => {
  const startDate = new Date();
  const endDate = new Date(new Date().setDate(startDate.getDate() + 7));
  date.value = [startDate, endDate];
  return Date;
});
</script>

<template>
  <NavbarSidebar />
  <div class="inner">
    <!-- 內容區 -->
    <div class="container-fluid main">
      <button type="button" class="btn btn-primary confirm-btn">Confirm</button>
      <button type="button" class="btn btn-primary cancel-btn">Cancel</button>

      <!-- 下拉式選單 -->
      <div class="dropdown">
        <button
          class="btn btn-secondary dropdown-toggle"
          type="button"
          id="dropdownMenuButton1"
          data-bs-toggle="dropdown"
          aria-expanded="false"
        >
          下拉式選單
        </button>
        <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
          <li><a class="dropdown-item" href="#">選項一</a></li>
          <li><a class="dropdown-item" href="#">選項二</a></li>
          <li><a class="dropdown-item" href="#">選項三</a></li>
        </ul>
      </div>

      <!-- 日期選擇套件 Vue3-Datepicker -->
      <Datepicker class="datepicker" v-model="date" range />

      <!-- 白色內容方塊 -->
      <div class="content-box">
        <p class="title"><strong>測試標題</strong></p>
        <hr />
        <p>測試用內文</p>
        <button type="button" class="btn btn-primary confirm-btn">test</button>
      </div>

      <div class="content-box-border">
        <p class="title"><strong>測試標題</strong></p>
        <hr />
        <p>測試用內文</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.inner {
  position: fixed;
  margin-top: 130px;
  margin-left: 300px;
  margin-right: 50px;
  background-color: #fff;
}
@media (max-width: 850px) {
  .inner {
    margin-left: 250px;
    margin-right: 50px;
  }
}
@media (max-width: 768px) {
  .inner {
    margin-left: 200px;
    margin-right: 50px;
  }
}
@media (max-width: 650px) {
  .inner {
    margin-left: 150px;
    margin-right: 50px;
  }
}
</style>
