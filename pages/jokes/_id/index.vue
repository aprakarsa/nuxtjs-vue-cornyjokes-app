<template>
    <div>
        <nuxt-link to="/jokes">&lt;&lt; Back to Jokes list</nuxt-link>
        <br><br>
        <h3>{{ joke }}</h3>
        <hr>
        <small>joke id: {{ $route.params.id }}</small>    
    </div>
</template>

<script>
import axios from 'axios';

export default {
    data() {
        return {
            joke: {}
        }
    },
    async created() {
        const config = {
            headers: {
                'Accept': 'application/json'    
            }
        }
        try {
            const res = await axios.get(`https://icanhazdadjoke.com/j/${ this.$route.params.id }`, config);

            this.joke = res.data.joke;
            // console.log(res.data)
            
        } catch (err) {
            console.log(err);
        }
    }
}
</script>

<style>
</style>