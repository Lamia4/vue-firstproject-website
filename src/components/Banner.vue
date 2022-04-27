<template>
    <div>
        <img class="bannerAnime" :src="urlAnime"/>
        <h1 class="titlebanner">{{ message }}</h1>
  </div>
</template>

<script>
    export default {
        data() {
        return {
            urlAnime: "https://girlsincapes.com/wp-content/uploads/2021/09/Demon-Slayer-04-Entertainment-District-wide.png"
        }
    },
    props:["message"]
    
    }

</script>