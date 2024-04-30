<template>
    <div id="header">
        <ul>
            <li class="menu-item" v-for="item in Cosas">{{ item  }}</li>
        </ul>
    </div>
</template>
<script setup>
const Cosas = ["Inicio", "Sobre mí", "Contacto"]
</script>
<style>
    #header{
        padding: 20px;
    color:rgb(255, 230, 0);
    text-align: center;
    transition: background-color 0.5s, color 0.3s;
    border: 1px solid #ee05cf;
    border-radius: 10px;
    margin: 14px 155px 0px 155px;
    
    
    }
    .menu-item {
    display: inline-block;
    margin: 0 10px;
    cursor: pointer;
    font-weight: bold;
    transition: color 0.3s;
}

.menu-item:hover {
    color: #ee05cf;
}
</style>