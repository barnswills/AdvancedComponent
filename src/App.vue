<template>
  <div id="app">
    <h1>Advanced Component</h1>
    <app-quote quote="a better quote">
      <h2 slot="title">{{quoteTitle}}</h2>
      <p>Wonderful world...</p>
    </app-quote>
  </div>
</template>

<script>
import Quote from "./components/Quote";

export default {
  name: "App",

  data: () => {
    return { quoteTitle: "The Quote"}
  },
  components: { appQuote: Quote }
};
</script>

<style scoped>
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  h2 {
    color: red;
  }
</style>
