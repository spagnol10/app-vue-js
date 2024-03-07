<template>
  <div>
    <h1 :class="{ 'title' : true, 'title-home' : isHome}">
      Curso VueJs
    </h1>

    <div v-for="(obj, index) in todos" :key="obj.id" class="todos-item">
      {{ index }} - {{ obj.text }}
    </div>

    <p class="paragrafo">
      Lora ipsum dolor sit amet, consectetur adipiscing elit. 

    </p>
</div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      isHome: false,
      classTitle: "title",
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
        {
          id: 3,
          text: "Play around in JSFiddle",
          done: true,
        },
        {
          id: 4,
          text: "Build something awesome",
          done: true,
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.paragrafo {
  color: #42b983;
  font-size: 2rem;
}

.title-home {
  color: #fd0000;
}

.title {
  font-size: 2rem;
  text-align: center;
  color: #42b983;
}

.todos-item {
  margin: 10px;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #000000;
  color: #fff;
}
</style>
