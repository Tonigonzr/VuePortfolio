<template>
    <div id="header">
      <ul>
        <li class="menu-item" v-for="item in Cosas" :key="item">{{ item }}</li>
      </ul>
    </div>
    <div id="theme-changer" class="theme-changer animate-in">
      <div id="thread" class="thread">
        <div
          id="theme-changer-toggle"
          class="sign"
          :class="tema === 'claro' ? 'sun' : 'moon'"
          @click="cambiarTema"
        ></div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const Cosas = ["Inicio", "Sobre mí", "Contacto"];
  
  const tema = ref('claro'); // Inicialmente en modo claro
  
  function cambiarTema() {
    const body = document.body;
    body.classList.remove(tema.value === 'claro' ? 'tema-claro' : 'tema-oscuro');
    tema.value = tema.value === 'claro' ? 'oscuro' : 'claro';
    body.classList.add(tema.value === 'claro' ? 'tema-claro' : 'tema-oscuro');
  }
  </script>
  
  <style>
  /* Estilo para el cuerpo con transiciones suaves */
  body.tema-claro {
    background-color: rgb(216, 200, 214); /* Fondo claro */
    color: black; /* Texto negro */
    transition: background-color 0.5s, color 0.5s; /* Transición suave */
  }
  
  body.tema-oscuro {
    background-color: black; /* Fondo oscuro */
    color: white; /* Texto blanco */
    transition: background-color 0.5s, color 0.5s; /* Transición suave */
  }
  
  .theme-changer {
    position: absolute;
    right: max(5%, 50px);
    z-index: 3;
    top: -55px;
  }
  
  .thread {
    display: inline-block;
    height: 160px;
    width: 2px;
    background: #7e5437;
    transform-origin: 50% 0;
    border-radius: 5px;
    animation: pendulum 4.5s ease-in-out infinite;
  }
  
  .sign {
    width: 52px;
    height: 52px;
    cursor: pointer;
    position: absolute;
    bottom: -10px;
    left: -24px;
    background-size: cover;
    transition: transform 0.5s ease-in-out; /* Transición para el giro */
  }
  
  .sign.sun {
    background-image: url("https://codingpotions.com/assets/images/sign_sun.png");
    transform: rotateY(0deg); /* No rotación para el sol */
  }
  
  .sign.moon {
    background-image: url("https://codingpotions.com/assets/images/sign_moon.png");
    transform: rotateY(180deg); /* Rotación hacia atrás para la luna */
  }
  
  @keyframes pendulum {
    0%,
    100% {
      transform: rotate(7deg);
    }
    50% {
      transform: rotate(-7deg);
    }
  }
  
  @keyframes bounceInDown {
    0%,
    60%,
    75%,
    90%,
    100% {
      transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
    }
    0% {
      transform: translate3d(0, -3000px, 0);
    }
    60% {
      transform: translate3d(0, 25px, 0);
    }
    75% {
      transform: translate3d(0, -10px, 0);
    }
    90% {
      transform: translate3d(0, 5px, 0);
    }
    100% {
      transform: none;
    }
  }
  
  #header {
    padding: 20px;
    text-align: center;
    transition: background-color 0.5s, color 0.5s;
    border: 4px solid #ee05cf;
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
  