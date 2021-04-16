<template>
    <div>
        <h1>About the app</h1>
        <p>Very corny dad jokes, from <a href="https://icanhazdadjoke.com/api" target="_blank">this website</a> :-) made by <a href="https://nuxtjs.org/" target="_blank" class="nuxtGreenColor">nuxtjs</a>. Click on the jokes menu upper right menu and enjoy the corny jokes.</p>
    </div>
</template>

<script>
export default {
    head() {
        return {
            title: 'About the app',
            meta: [
                {
                    hid: 'description',
                    name: 'Description',
                    content: 'Best place for corny dad jokes'
                }
            ]
        }
    }
}
</script>

<style>
.nuxtGreenColor {
    color:#41b883;
}
a {
    text-decoration: underline;
    color:steelblue;
}
</style>