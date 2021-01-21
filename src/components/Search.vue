<template>
  <div class="search">
    <input
      type="text"
      v-model="query"
      @keypress.enter="handleSearch"
      placeholder="Lütfen Giph Giriniz..."
    />
    <button @click="handleSearch">Search</button>
  </div>
</template>

<script>
export default {
  name: "search",
  data() {
    return {
      query: "",
    };
  },
  methods: {
    handleSearch() {
      this.$emit("SearchRequested", this.query);
    },
  },
};
</script>

<style lang='scss'>
body {
  background-color: rgb(240, 236, 236);
  .search {
    text-align: center;
    margin: 50px 5px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    align-items: center;
    input {
      padding: 10px 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 28px;
      width: 500px;
      height: 30px;
      margin-bottom: 20px;
    }
    button {
      padding: 7px 15px;
      border: 1px solid #ccc;
      background-color: #4183c4;
      color: #fff;
      font-size: 16px;
      border-radius: 5px;
      font-size: 28px;
    }
  }
}
</style>
