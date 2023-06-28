<script>
export default {
    data() {
        return {
            picName: 'Napoli-scaled'
        }
    },
    methods: {
        getImagePath(picName) {
            const url = new URL(`../assets/${picName}.jpeg`, import.meta.url)
            return url.href;
        }
    }
}
</script>

<template>
    <img :src="getImagePath(picName)" alt="Campioni">
</template>

<style>
img {
    height: 600px;
    width: 900px;
}
</style>