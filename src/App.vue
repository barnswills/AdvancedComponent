<template>
  <div id="app">
    <h1>#1 Advanced Component</h1>
    <button @click="selectedComponent = 'appQuote'">Quote</button>
    <button @click="selectedComponent = 'appAuthor'">Authour</button>
    <button @click="selectedComponent = 'appNew'">New</button>
    <hr>
    <p>{{ selectedComponent }}</p>
    <keep-alive>
        <component :is="selectedComponent">
          <p>Default Content</p>
      </component>
    </keep-alive>
    
    <!-- <app-quote quote="a better quote">
      <h2 slot="title">{{quoteTitle}}</h2>
      <p>Wonderful world...</p>
    </app-quote> -->
  </div>
</template>

<script>
import Quote from "./components/Quote";
import New from "./components/New";
import Author from "./components/Author";

export default {
  name: "App",

  data: () => {
    return { quoteTitle: "The Quote", selectedComponent: "appQuote" };
  },
  components: { appQuote: Quote, appAuthor: Author, appNew: New }
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
