<template>
  <div class>
    <div class="card">
      <div class="container">
        <img class="avatarka" alt="Vue logo" src=".\..\src\assets\ava.png" />
        <h1>Багатов Ахмед</h1>
        <h2>ББСО-02-19</h2>
      </div>
      <div class="skills">
        <h1>Изучает JS</h1>
      </div>
    </div>
    <scan @mouseover="changeText"> Наведи сюда </scan>
    <p>{{ tit }}</p>
    <p :class="StyleCSS">Цвет: {{ StyleCSS }}</p>
    <input type="text" @input="StyleCSS = $event.target.value" />

    <br />
    <br />

    <button v-on:click="counter += 1">+1</button>
    <p>Кнопка выше была нажата {{ counter }} раз</p>
    <button
      class="vk"
      onclick="window.location.href = 'https://vk.com/bokoki';"
    >
      <img src=".\..\src\assets\vk.png" />
    </button>

    <br />
    <br />

    <input type="text" @input="increment($event.target.value)" />
    <p>{{ value }}</p>
    <p>{{ doublevalue }}</p>

    <br />
    <br />

    <button v-on:click="show = !show">Скрыть / показать</button>
    <p v-if="show">Невидимка абабабаб</p>
  </div>
</template>

<script>
export default {
  name: "AboutPage",
  data: () => ({
    tit: "hello world",
    StyleCSS: "",
    counter: 0,
    value: 1,
    show: true,
  }),
  methods: {
    changeText() {
      this.tit = "Магия :)";
    },
    increment(value) {
      this.value = value;
      //this.doublevalue = this.value * 2
    },
  },
  computed: {
    doublevalue() {
      return this.value * 2;
    },
  },

  components: {},
};
</script>

<style>
.vk {
  width: 60px;
  height: 60px;
  text-align: center;
  margin: 0 auto;
}

.avatarka {
  width: 100%;
}

.card {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fa0202;
  margin-top: 60px;
  width: 30%;
  margin: 0 auto;
}

.container {
  background: #32fc00;
  border-width: 2;
  border-radius: 5px;
  padding: 2px 8px;
}
.container:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.skills {
  background: #1c7a4e;
  border-width: 2;
  border-radius: 5px;
}
.skills:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.dsa {
    margin: 0%;
}
</style>
