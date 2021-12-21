<template>
  <div>
    <h1>This is my football app</h1>
    <h2>Here is a list of teams in the premier league:</h2>
    <Player 
      v-for="product in products.teams" 
      :product="product" 
      :key="product.name"
    />
  </div>
</template>

<script>
export default {
  async fetch() {
    this.products = await fetch("https://fantasy.premierleague.com/api/bootstrap-static/").then(
      (res) => res.json(),
    )
  },
  data() {
    return {
      products: {},
    }
  },
}
</script>
