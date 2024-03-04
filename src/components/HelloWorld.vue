<template>
  <div>
    <div v-for="(obj, index) in todos" v-bind:key="obj.id" class="todos-item">
      <img v-if="obj.img" v-bind:src="obj.img" />
      {{ index }} - {{ obj.text }}
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      todos: [
        {
          id: 1,
          text: "Learn JavaScript",
          done: false,
          img: "https://picsum.photos/200/300",
        },
        {
          id: 2,
          text: "Learn Vue",
          done: false,
          img: "https://picsum.photos/200/300",
        },
        { id: 3, text: "Play around in JSFiddle", done: true },
        { id: 4, text: "Build something awesome", done: true },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.todos-item {
  margin: 10px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #000000;
  color: #fff;
}
</style>
