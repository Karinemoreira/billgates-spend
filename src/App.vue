<template>
  <header>
    <span>Neal.fun</span>
  </header>
  <CardTitle msg="Welcome to Your Vue.js App" />
  <div class="money-bar">{{ spend }}</div>
  <div>
    <product-card
      v-for="product in products"
      :key="product.name"
      :name="product.name"
      :price="product.price"
    />
  </div>
</template>

<script>
  import CardTitle from "./components/CardTitle.vue";
  import ProductCard from "./components/ProductCard.vue";

  export default {
    name: "App",
    components: {
      CardTitle,
      ProductCard,
    },
    data() {
      return {
        spend: "$100,000,000,000",
        products: [
          { image: "", name: "Pizza", price: "$9" },
          { image: "", name: "Macarrão", price: "$29" },
          { image: "", name: "Lasanha", price: "$19" },
          { image: "", name: "Sorvete", price: "$3" },
          { image: "", name: "Soda", price: "$1" },
          { image: "", name: "Camarão", price: "$5" },
          { image: "", name: "Sopa", price: "$2" },
        ],
      };
    },
  };
</script>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
  }

  body {
    background-color: #f1f2f6;
  }

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background-color: #f1f2f6;
  }
  header {
    font-size: 30px;
    font-weight: 700;
    padding: 30px 0 30px 15px;
    background-color: #fff;
    margin-bottom: 25px;
    display: flex;

    span {
      color: #333;
      background: #fff;
    }
  }

  .money-bar {
    color: #fff;
    background-color: #2ecc71;
    background: linear-gradient(180deg, #2ecc71, #1abc9c);
    padding: 20px;
    margin: 10px 0;
    font-family: Roboto, sans-serif;
    font-size: 32px;
    font-weight: 700;
    text-align: center;
    top: 0;
    position: sticky;
    z-index: 9999;
  }
</style>
