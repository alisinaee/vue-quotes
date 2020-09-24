<template>
  <div class="container">
    <newQuote-cmp @newQuote="addQuote"></newQuote-cmp>
    <quotesGrid-cmp :quotes="quotes" :deleteQouteFn="deleteQuote"></quotesGrid-cmp>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">info : click an item to delete from list!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuotesGrid from "./components/quoteGrid";
import NewQuote from "./components/newQuote";

export default {
  components: {
    "quotesGrid-cmp": QuotesGrid,
    "newQuote-cmp": NewQuote,
  },
  data: function () {
    return {
      quotes: ["this is simple of quote !"],
      maxQ: 10,
    };
  },
  methods: {
    addQuote(quote) {
      this.quotes.push(quote);
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    },
  },
};
</script>

<style>
</style>
