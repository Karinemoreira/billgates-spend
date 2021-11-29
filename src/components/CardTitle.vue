<template>
  <div class="container">
    <img
      class="container__img"
      src="../assets/billgates.jpg"
      alt="Foto do Bill Gates"
    />
    <h1>Spend Bill Gates' Money</h1>
  </div>
</template>

<script>
  export default {
    name: "CardTitle",
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .container {
    background-color: #ffffff;
    font-size: 32px;
    padding: 30px 20px;
    margin-bottom: 10px;
    font-weight: 700;
    text-align: center;
    line-height: 1.3em;
    img {
      user-select: none;
      width: 125px;
      height: 125px;
      margin: 10px auto 25px;
      border-radius: 125px;
    }
    h1 {
      margin-bottom: 10px;
    }
  }
</style>
