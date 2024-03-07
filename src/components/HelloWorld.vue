<template>
  <div class="home">
    <div class="form">
      <input v-model="name" type="text" />
      <button>Submit</button>

      <br />

      {{ name }}

      <br />
      <br />
      <br />

      <div>
        <label>Sports</label>
        <br />
        <select v-model="sports">
          <option value="">Escolha</option>
          <option value="Soccer">Soccer</option>
          <option value="Basketball">Basketball</option>
          <option value="Baseball">Baseball</option>
        </select>
      </div>

      <br />
      <br />

      <div>
        <label>Escolha</label>

        <br />
        <input type="radio" v-model="newLetter" value="Sim" /> Sim
        <input type="radio" v-model="newLetter" value="Não" /> Não

        <br />
        {{ newLetter }}
      </div>

      <br />

      <div>
        <label for="">Contrato</label>
        <br />
        <input v-model="contract" type="checkbox" />
        Aceita nossos termos?
      </div>
      {{ contract }}
    </div>

    <div>
      <button @click="onClick()">click</button>
    </div>

    <br />

    <div @mouseover="mouseOver()"
          @mouseout="mouseOut()">
      Mouse
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      contract: false,
      newLetter: "",
      name: "John Doe",
      sports: "",
      // sports: ["Soccer", "Basketball", "Baseball"],
    };
  },

  methods: {
    onClick() {
      console.log("Clicked");
    },

    mouseOver() {
      console.log("Mouse over");
    },
    mouseOut() {
      console.log("Mouse Out");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home {
  margin: 20px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  background-color: #f9f9f9;
  color: #333;
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  text-align: center;
  width: 50%;
  margin: 0 auto;
  margin-top: 50px;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  background-color: #f9f9f9;
  color: #333;
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  text-align: center;
  width: 50%;
  margin: 0 auto;
  margin-top: 50px;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  background-color: #f9f9f9;
  color: #333;
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  text-align: center;
  width: 50%;
  margin: 0 auto;
  margin-top: 50px;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  background-color: #f9f9f9;
  color: #333;
  font-family: Arial, sans-serif;
  font-size: 16px;
  line-height: 1.6;
  text-align: center;
  width: 50%;
  margin: 0 auto;
  margin-top: 50px;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>
