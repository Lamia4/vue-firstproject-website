<template>
    <div>
        <div class="item">

            <h2>{{ item }}</h2>
       <img :src="url" width="235" height="300"/>
       <div class="quantity">
         <button class="inc" @click="counter > 0 ? counter -= 1 : 0">-</button>
         <span class="quant-text">Quantity: {{ counter }}</span>
         <button class="inc" @click="counter += 1">+</button>
       </div>
       <button class="submit">Add to cart</button>
        </div>
  </div>
</template>

<script>
    export default {
        data() {
        return {
            counter: 0,
            urlAnime: "https://girlsincapes.com/wp-content/uploads/2021/09/Demon-Slayer-04-Entertainment-District-wide.png"
        }
    },
    props: ["item", "url"],
    }

</script>