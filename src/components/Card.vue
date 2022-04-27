<template>
<div class="card">
    <span class="img"></span>
    <h1>Rosa Duarte</h1>
    <p>Web developer | JavaScript | Vue.js | PHP</p>
    <social-media />
</div>
</template>

<script>
import SocialMedia from '@/components/SocialMedia.vue'

export default {
    components: {SocialMedia},
    props: ['mode']
}
</script>

<style scoped>
.dark .card{
    background-color: #3D5A73;
    border: 1px solid var(--blue);
    box-shadow: 0 0 5px var(--sand);
}
.card{
    width: 300px;
    min-width: 290px;
    height: 450px;
    border: 1px solid var(--old-pink);
    border-radius: 20px;
    color: var(--light-blue);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    text-align: center;
    padding: 20px;
    background-color: var(--sand);
    box-shadow: 0 0 5px var(--red-wine);
}
.img{
    background-image: url("../assets/image/img.jpg");
    background-size: cover;
    width: 180px;
    height: 180px;
    border-radius: 50%;
    margin: 0 auto;
    border: 2px solid var(--light-blue);
}
.card h1{
    font-weight: 700;
}
.card p{
    margin-bottom: 20px;
    font-size: 20px;
    font-weight: 500;
}
</style>