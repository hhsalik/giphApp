<template>
  <div id="preview">
    <ul>
      <li v-for="gif in gifs" :key="gif">
        <img :src="gif.images.fixed_height.url" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "preview",
  props: ["gifs"],
};
</script>

<style lang="scss">
#preview {
  li {
    list-style: none;
    float: left;
    margin: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      border-radius: 5px;
      border: 1px solid black;
    }
  }
}
</style>
