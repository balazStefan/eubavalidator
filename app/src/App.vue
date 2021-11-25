<template>
  <div>
    <h1>Citácie Euba</h1>
    <input type="text" placeholder="Krsné meno authora" v-model.trim="name" />
    <input
      type="text"
      placeholder=" Priezvisko authora"
      v-model.trim="priezvisko"
    />
    <input type="text" placeholder="Názov diela" v-model.trim="dielo" />
    <input type="text" placeholder="Mesto" v-model.trim="mesto" />
    <input type="text" placeholder="Vydavateľ" v-model.trim="vydavatel" />
    <input type="text" placeholder="Rok vydania" v-model.trim="rok" />
    <input type="text" placeholder="Strany" v-model.trim="strany" />

    <input
      type="text"
      placeholder="Štandartné číslo"
      v-model.trim="standartcislo"
    />
    <p>
      {{
        priezvisko.toUpperCase() +
        ", " +
        name.toLowerCase().charAt(0).toUpperCase() +
        name.slice(1) +
        ". " +
        dielo.toLowerCase().charAt(0).toUpperCase() +
        dielo.slice(1) +
        ". " +
        mesto.toLowerCase().charAt(0).toUpperCase() +
        mesto.slice(1) +
        " : " +
        vydavatel.toLowerCase().charAt(0).toUpperCase() +
        vydavatel.slice(1) +
        ", " +
        rok +
        ". " +
        "s." +
        strany +
        ". " +
        standartcislo +
        "."
      }}
    </p>
    <p class="note">
      Font je nadstavený na : Times New Roman na 12px čo by malo odpovedať
      štandartom, stačí len nakopírovať 😎
    </p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      priezvisko: "",
      dielo: "",
      rok: "",
      vydavatel: "",
      mesto: "",
      strany: "",
      standartcislo: "",
    };
  },
};
</script>
<style scoped>
div {
  font-family: "Times New Roman", Times, serif;
  font-size: 12px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  /* border: 2px solid black; */
}

input {
  width: 250px;
  padding: 0.5rem;
  margin-bottom: 0.5rem;
}
.note {
  font-size: 1rem;
}
strong {
  font-size: 1rem;
  margin-right: 1rem;
}
div {
  width: 75rem;
  height: fit-content;
  margin: 5rem auto;
  color: #555d50;
  box-shadow: 0.8rem 0.4rem #ccc;
  border-radius: 0.9rem;
  border: 0.1rem solid #ccc;
  background-color: white;
}
</style>
