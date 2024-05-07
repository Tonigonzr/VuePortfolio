<template>
  <div class="container">
    <div class="header-flex">
      <!-- Imagen a la izquierda del título -->
      <img id="imgProfileLeft" src="https://media1.tenor.com/m/ZAMoMuQgf9UAAAAC/mapache-pedro.gif" alt="Perfil Izquierda" />
      <!-- Título centrado -->
      <h1>Mi Portfolio</h1>
      <!-- Imagen a la derecha del título -->
      <img id="imgProfileRight" src="https://media1.tenor.com/m/ZAMoMuQgf9UAAAAC/mapache-pedro.gif" alt="Perfil Derecha" />
    </div>
    
    <p>Bienvenido a mi portfolio. Aquí puedes encontrar información sobre mis proyectos.</p>
    <div>
      <h2 id="title-h2">Proyectos</h2>
    </div>
    <div class="proyectos">
      <!-- Proyecto 1 -->
      <div class="tarjeta-proyecto">
        <h3>TicketService</h3>
        <img id="img-project"src="https://cdn-icons-png.flaticon.com/512/785/785581.png" alt="Proyecto 1" />
        <p>Una aplicación web para gestionar el soporte de una empresa mediante tickets.</p>
        <img id="icon-language-projects2" src="https://seeklogo.com/images/F/flutter-logo-5086DD11C5-seeklogo.com.png" alt="">
        <img id="icon-language-projects2" src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Firebase_icon.svg/2048px-Firebase_icon.svg.png" alt="">
      </div>

      <!-- Proyecto 2 -->
      <div class="tarjeta-proyecto">
        <h3>Juego Pokemon Java</h3>
        <img id="img-project" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/Pok%C3%A9_Ball_icon.svg/1200px-Pok%C3%A9_Ball_icon.svg.png" alt="Proyecto 2" />
        <p>Juego de pokemon hecho con lenguaje java como proyecto final de 1ºDAM</p>
        <img id="icon-language-projects" src="https://cdn-icons-png.flaticon.com/512/226/226777.png" alt="">
      </div>

    </div>
  </div>
</template>

<style>
#title-h2{
  display: -webkit-box;
  display: flex;
  -webkit-box-align: center;
          align-items: center;
  -webkit-box-pack: center;
          justify-content: center;
  background-repeat: repeat-y;
  background-position: center center;
  background-size: cover, 100% 3px;
  font-size: 34px;
  font-family: 'VT323', monospace, sans-serif;
  color: #3f3;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
#icon-language-projects2{
  margin: 15px 12px 0px 0px;
  width: 30px;
}
#icon-language-projects{
  margin: 15px 0px 0px 0px;
  width: 35px;
}
#img-project{
  width: 150px;
  margin: 25px 0px 20px 0px ;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

.header-flex {
  display: flex; /* Usar flex para alinear elementos horizontalmente */
  justify-content: center; /* Centrar el contenido */
  align-items: center; /* Centrar verticalmente */
  gap: 10px; /* Ajustar la distancia entre elementos */
}

h1 {
  color: #f72585; /* Morado neón */
  font-size: 2em;
  margin: 0; /* Sin margen para mantener el centro */
  text-align: center; /* Asegurar que el texto del título esté centrado */
}

p {
  font-size: 1.2em;
  line-height: 1.6;
  text-align: center; /* Texto centrado */
}

#imgProfileLeft,
#imgProfileRight {
  border-radius: 50px;
  width: 40px; /* Tamaño pequeño */
  height: 40px; /* Tamaño pequeño */
}

h2 {
  text-align: center;
  color: #7209b7; /* Morado oscuro */
  font-size: 1.5em;
  margin: 15px 0 20px 0;
}

.proyectos {
  display: flex;
  flex-wrap: wrap;
  gap: 20px; /* Espacio entre tarjetas */
  justify-content: center; /* Centrar las tarjetas */
}

.tarjeta-proyecto {
  background: #f4f4f4;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 15px;
  width: 250px;
  text-align: center;
  transition: transform 0.3s;
}

.tarjeta-proyecto:hover {
  transform: scale(1.05); /* Efecto de hover */
}

.tarjeta-proyecto h3 {
  color: #d00000; /* Rojo para el título de los proyectos */
}

.tarjeta-proyecto img {
  width: 100%; /* Imagen ajustada a la tarjeta */
  border-radius: 10px;
}

.tarjeta-proyecto p {
  font-size: 1em;
  color: #333; /* Texto gris oscuro */
}
</style>
