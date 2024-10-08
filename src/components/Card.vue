<template>
  <div class="card shadow-sm">
    <span class="img" :style="{backgroundImage: `url(${item.imgPath})`}" />
    <div class="card-body">
      <p class="card-text">{{item.name}}</p>
      <div class="d-flex justify-content-between align-items-center">
        <div class="btn-group">
          <button class="btn btn-primary">주문하기</button>
        </div>
        <small class="text-body-secondary">{{libs.getNumberFomatted(item.price)}}원</small>
      </div>
    </div>
  </div>
</template>

<script>
import libs from "@/scripts/libs";

export default {
  name: "Card",
  props:{
    item: Object
  },
  setup(){
    return {libs}
  }

}
</script>

<style scoped>
.card {
  font-family: 'Pretendard-Regular';
  .card-text {
    font-size: 25px;
  }
}
.card .img {
  width: 100%;
  display: inline-block;
  height: 300px;
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}
</style>