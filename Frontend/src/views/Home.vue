<template>
  <div class="home-container">
    <div class="intro">
      <h1>Hola, soy Nina</h1>
      <p>
        En este portafolio presentaré los proyectos que he realizado que creo que son más significativos y que han tenido mayor impacto en mi formación como estudiante en computación.<br>
        Antes de empezar, hay que tomar en cuenta que esta pagina se realizó con Vue y levanté mi propio servidor para poder mostrar todo.<br>
        El dominio es <strong>namarak.space</strong>
      </p>
      <p>
        Enlace al repositorio de GitHub del portafolio: 
        <strong>
            <a href="https://github.com/Ninaswiftie09/Portafolio_Nina" target="_blank" rel="noopener noreferrer" class="custom-link">
            https://github.com/Ninaswiftie09/Portafolio_Nina
            </a>
        </strong>
        </p>

      <img
        src="https://i.pinimg.com/originals/8b/19/fe/8b19feb0d9eec43509283e74917a7fe9.gif"
        alt="Intro Gif"
        class="intro-gif"
      />
    </div>
    <div class="projects">
      <h2>Proyectos Destacados</h2>
      <div class="grid">
        <ProjectCard
          v-for="project in projects"
          :key="project.name"
          :project="project"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import ProjectCard from '../components/ProjectCard.vue'

const projects = [
  { name: 'Juego de Snake', repo: 'https://github.com/Ninaswiftie09/Pry3MicrosSnake' },
  { name: 'Ur Music', repo: 'https://github.com/Ninaswiftie09/UrMusic' },
  { name: 'Renta de Autos', repo: 'https://github.com/Ninaswiftie09/Proyecto3_BD' },
  { name: 'Calculadora Mejor Ruta', repo: 'https://github.com/Ninaswiftie09/Mejor_Ruta' },
  { name: 'Calculadora usando Componentes', repo: 'https://github.com/Ninaswiftie09/Proyecto1_SW' },
  { name: 'Monty Hall', repo: 'https://github.com/JoseOrdonezB/proyecto-probabilidades' },
  { name: 'Swift Vision', repo: 'https://github.com/Ninaswiftie09/SwiftVision' },
  { name: 'Botón SOS', repo: 'https://github.com/Ninaswiftie09/Proyecto_PlataformasMoviles' },
  { name: 'Juego de Memoria', repo: 'https://github.com/Ninaswiftie09/lab7SW' },
  { name: 'Chat', repo: 'https://github.com/Ninaswiftie09/chat_sw' },
  { name: '¿Quién Mató a Cristiano?', repo: 'https://github.com/Ninaswiftie09/QuienMatoaCristiano' },
  { name: 'Enscriptación RSA', repo: 'https://github.com/Ninaswiftie09/encriptacionRSA' },
  { name: 'BOF', repo: 'https://github.com/Ninaswiftie09/BOF' }
]
</script>

<style scoped>
.home-container {
  display: flex;
  height: 100vh;      
  width: 100vw;       
  background: url('https://i.pinimg.com/originals/fd/b2/1c/fdb21c0e4f3dbb6ccd9a63c68fce8645.gif') no-repeat center center fixed;
  background-size: cover; 
  gap: 1rem;
  color: #dbe5ff;
  font-family: 'Poppins', sans-serif;
  text-shadow: 0 0 8px rgba(35, 51, 95, 0.8);
  box-sizing: border-box;
}


.intro {
  flex: 1;
  max-width: 45%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.intro h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  color: #9bb7ff;
  text-shadow: 0 0 15px #7086ff;
}

.intro p {
  font-size: 1.15rem;
  line-height: 1.6;
  margin-bottom: 2rem;
  color: #c3d0ffdd;
}

.intro strong {
  color: #a2b9ff;
}

.intro-gif {
  width: 100%;
  max-width: 320px;
  border-radius: 16px;
  box-shadow: 0 0 20px #8aa2ffaa;
  align-self: center;
  user-select: none;
}

.projects {
  flex: 1.2;
  max-width: 55%;
  overflow-y: auto;
  padding-right: 1rem;
}

.projects h2 {
  font-size: 2.4rem;
  margin-bottom: 1.8rem;
  color: #8aa2ff;
  text-shadow: 0 0 12px #5478ffcc;
  font-weight: 700;
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
}

.projects::-webkit-scrollbar {
  width: 10px;
}

.projects::-webkit-scrollbar-thumb {
  background: #6f8fffaa;
  border-radius: 8px;
}

.projects::-webkit-scrollbar-thumb:hover {
  background: #8aa2ffbb;
}

.projects::-webkit-scrollbar-track {
  background: transparent;
}

@media (max-width: 900px) {
  .home-container {
    flex-direction: column;
    height: auto;
  }
  .intro, .projects {
    max-width: 100%;
  }
  .projects .grid {
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  }
  .intro-gif {
    max-width: 100%;
  }
}

.custom-link {
  color: #003366;
  text-decoration: underline;
}

.custom-link:hover {
  color: #00509e;
}

</style>
