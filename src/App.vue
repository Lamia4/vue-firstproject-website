<template>
  <div id="app">
  <div>
    <mainmenu></mainmenu>
    <banner :message="message"></banner>
    <div class="flexrow">
      <div class="unit" v-for="unit in manifest">
        <child :item="unit.item" :url="unit.url"></child>
      </div>
    </div>
  </div>
</div>
</template>

<script>
  import Mainmenu from "./components/Mainmenu.vue";
  import Child from "./components/Child.vue";
  import Banner from "./components/Banner.vue";
export default {

  components: {
    Child,
    Mainmenu,
    Banner
  },
  name: 'app',
  data () {
    return {
      message: "Choose your favorite",
      manifest: [
        {
          item: "Naruto Shippuden - Poster",
          url: "https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcQufPumJV7EIGpk0qUwNJGcVEkMsuJgShEuTUZjQBpIyRbjOZSc32BGsr1xKzVzCgAIUiIeCG-IAtc1SswhTl3QteDmUFEmArqbJlt3PiE9wRAf3fJ7JSsdMQ&usqp=CAE"
        },
        {
          item: "Jujutsu Kaisen - Plush",
          url: "https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcTUuEmPe1tScpLfXlHtZ92IBAOCQ8P8f3y4MgwRl3zJS5SIa9MPBtJtrSuelFDWr1WUM3HEZ9xQ7B8Bi1KQC2AttpL7JspZV4flafHGaE7MAS8bthVSHICgIA&usqp=CAE"
        },
         {
          item: "Demon Slayer - Sword Zenitsu",
          url: "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcTFJvci1gboGp2K6q9zgRZcoKz-71V6BmUcf8cqjendcmvrc6qr-7Ho-CJU0iLZ6lwlq14t568CsdmxvJvmQRa7kmEXK9FFKcYoNSO4FRtv0k2rvsruN1zkVw&usqp=CAE"
        },
      ]
    };
  }
}
</script>

<style>

body, html {
  font-family: "PT Serif", serif;
  background-color: rgb(36, 15, 88);
  margin: 0px;
  padding: 0px;
  width: 100vw;
}

.flexrow {
  display: flex;
  justify-content: center;
}

header {
  background: #222;
  padding: 30px 0px 10px 0px;
  width: 100vw;
  color: white;
  display: flex;
  align-content: center;
  justify-content: center;
  height: 80px;
  margin-left: 10px;
}
header ul {
  padding-left: 0;
}
header a {
  color: white;
  text-decoration: none;
  padding: 0 10px;
  transition: all 0.2s ease;
}
header a:hover {
  color: #E6534B;
}

.stamp {
  width: 30px;
  height: 30px;
  margin: 10px;
  float: left;
}

.cart {
  width: 40px;
  height: 40px;
  margin: 5px;
}

.special, h1, h2, h3, li {
  font-family: "Montserrat", sans-serif;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  font-size: 18px;
}

.quant-text, button.submit {
  font-size: 18px;
}

h2 {
  font-size: 20px;
  margin: 0 0 5px;
  text-align: center;
}

li {
  list-style: none;
  display: inline-block;
}

input {
  background: #eee;
}

button {
  border: none;
  border-radius: 1000px;
  padding: 8px 13px;
  outline: none;
  cursor: pointer;
  margin-top: 5px;
}
button.inc {
  background: white;
  color: black;
  font-size: 20px;
  font-weight: bold;
}
button.submit {
  background: black;
  color: white;
  margin-left: 20px;
  padding: 12px 14px;
  width: 240px;
}
button.submit:hover {
  opacity: 0.8;
  background-color: rgb(154, 32, 124);
  transition: all ease-out;
}

.quant-text {
  display: inline-block;
  text-align: center;
  width: 140px;
  padding: 8px;
}

.quantity {
  border: 2px solid black;
  width: 235px;
  padding-left: 3px;
  border-radius: 1000px;
  background: #fff;
  margin-left: 20px;
  margin-top: 5px;
}

.item {
  display: flex;
  flex-direction: column;
  width: 280px;
  height: 440px;
  justify-content: space-around;
  background: rgb(233, 218, 230);
  padding: 20px 10px;
  margin: 30px;
}
.item img {
  align-self: center;
}
.bannerAnime{
  height: 600px;
  padding: 0px 10px 0px 10px;
  width: 100vw;
}
.titlebanner {
  text-align: center;
  font-weight: bold;
  font-size: 38px;
  --shadow-color: #cd95c0;
  --shadow-color-light: rgb(213, 114, 219);
  color: rgb(154, 32, 124);
  animation: neon 3s infinite;
}


@keyframes neon {
  0% {
    text-shadow: -1px -1px 1px var(--shadow-color-light), -1px 1px 1px var(--shadow-color-light), 1px -1px 1px var(--shadow-color-light), 1px 1px 1px var(--shadow-color-light),
    0 0 3px var(--shadow-color-light), 0 0 10px var(--shadow-color-light), 0 0 20px var(--shadow-color-light),
    0 0 30px var(--shadow-color), 0 0 40px var(--shadow-color), 0 0 50px var(--shadow-color), 0 0 70px var(--shadow-color), 0 0 100px var(--shadow-color), 0 0 200px var(--shadow-color);
  }
  50% {
    text-shadow: -1px -1px 1px var(--shadow-color-light), -1px 1px 1px var(--shadow-color-light), 1px -1px 1px var(--shadow-color-light), 1px 1px 1px var(--shadow-color-light),
    0 0 5px var(--shadow-color-light), 0 0 15px var(--shadow-color-light), 0 0 25px var(--shadow-color-light),
    0 0 40px var(--shadow-color), 0 0 50px var(--shadow-color), 0 0 60px var(--shadow-color), 0 0 80px var(--shadow-color), 0 0 110px var(--shadow-color), 0 0 210px var(--shadow-color);
  }
  100% {
    text-shadow: -1px -1px 1px var(--shadow-color-light), -1px 1px 1px var(--shadow-color-light), 1px -1px 1px var(--shadow-color-light), 1px 1px 1px var(--shadow-color-light),
    0 0 3px var(--shadow-color-light), 0 0 10px var(--shadow-color-light), 0 0 20px var(--shadow-color-light),
    0 0 30px var(--shadow-color), 0 0 40px var(--shadow-color), 0 0 50px var(--shadow-color), 0 0 70px var(--shadow-color), 0 0 100px var(--shadow-color), 0 0 200px var(--shadow-color);
  }
}
</style>
