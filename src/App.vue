<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
</script>

<template>
    <div>
        <h1>{{ headline }}</h1>
    </div>
</template>

<script>
export default {
    name: 'App',
    data() {
        return {
            headline: 'Hello World',
        }
    },
}
</script>

<style>
body {
    margin: 0;
    font-family: monospace, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

#app {
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

h1 {
    font-size: clamp(16px, 10vh, 250px);
    font-weight: 700;
    line-height: 100%;
    color: #1f2a44;
}
</style>
