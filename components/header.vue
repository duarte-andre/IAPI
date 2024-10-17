<template>
  <div>
    <header :class="{ 'transparent': isTransparent }">
      <div class="interface" style="height: 65px; margin: 0px 25%;">
        <div class="logo" :class="{ 'hidden': isTransparent }">
          
            <h1 class="iapi" style="margin: 0px -325%; color:#0eacdb; con">IAPI</h1>
          
        </div>
        <nav class="menu-desktop" :class="{ 'hidden': isTransparent }">
          <ul>
            <li><a href="#topo-do-site">Início</a></li>
            <li><a href="#txt-topo">Sobre Nós</a></li>
            <li><a href="#especiliadades">Objetivos</a></li>
            <li><a href="#cultura">Projetos</a></li>
          </ul>
        </nav>
        <div class="btn-contato" :class="{ 'hidden': isTransparent }">
          <button>Contato</button>
        </div>
        <div class="overlay-menu" id="overlay-menu"></div>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isTransparent: false, // Estado do menu
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll); // Adiciona o listener de scroll
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll); // Remove o listener de scroll
  },
  methods: {
    handleScroll() {
      const scrollY = window.scrollY || window.pageYOffset;
      // Define o ponto em que o menu e os itens somem
      this.isTransparent = scrollY > 100; // Altere esse valor se necessário
    },
  },
};
</script>


<style>
/* FONTES E ÍCONES */
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900&display=swap");
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css");

/* RESET E ESTILO GERAL */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

.interface {
  max-width: 1300px;
  margin: 0 auto;
  padding: 0; /* Remover padding lateral */
}

/* FLEX LAYOUT */
.flex {
  display: flex;
}

.iapi {
  color: #ffffff; /* Cor do texto */
  text-shadow: 
    -2.5px -2.5px 0 #000000,  /* Contorno esquerdo superior */
     2.5px -2.5px 0 #000000,  /* Contorno direito superior */
    -2.5px  2.5px 0 #000000,  /* Contorno esquerdo inferior */
     2.5px  2.5px 0 #000000;  /* Contorno direito inferior */
}

/* BOTÃO DE CONTATO */
.btn-contato button {
  padding: 8px 30px;
  font-size: 18px;
  font-weight: 600;
  background-color: #0eacdb;
  border: 0;
  border-radius: 30px;
  cursor: pointer;
  transition: 0.2s;
  margin: 0 auto;
  display: block;
}

button:hover {
  box-shadow: 0px 0px 8px #0eacdb;
  transform: scale(1.05);
}

/* CABEÇALHO */
/* Estilo do cabeçalho */
header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 0; /* Remover padding */
  background-color: rgba(255, 255, 255, 1);
  transition: background-color 0.5s ease, opacity 0.5s ease;
  z-index: 1000;
}

/* Cabeçalho transparente */
header.transparent {
  background-color: rgba(255, 255, 255, 0); /* Transparente */
}

/* Itens do menu desaparecem quando transparente */
.hidden {
  opacity: 0;
  pointer-events: none; /* Evita interação quando invisível */
  transition: opacity 0.5s ease;
}

/* Interface e Layout */
header > .interface {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0;
  padding: 0; /* Ajustar margens e paddings */
}

/* MENU */
nav.menu-desktop {
  background-color: rgba(255, 255, 255, 0.9); /* Fundo branco com leve transparência */
  border-radius: 8px; /* Bordas arredondadas */
  padding: 10px; /* Espaçamento interno */
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1); /* Sombra suave */
}

/* Links do menu */
nav.menu-desktop a {
  text-decoration: none; /* Remove o sublinhado */
  color: #5c5c5c; /* Cor do texto */
  font-weight: 500; /* Peso da fonte */
  transition: color 0.3s ease, transform 0.3s ease; /* Transição suave */
}

/* Hover do menu */
nav.menu-desktop a:hover {
  color: #0eacdb; /* Cor ao passar o mouse */
  transform: translateY(-2px); /* Efeito de elevação */
}

/* Estilo do item do menu */
nav.menu-desktop ul li {
  display: inline-block;
  padding: 0 20px; /* Ajustar o espaçamento lateral */
  position: relative; /* Para adicionar efeitos como sublinhados */
}

/* Adicionando um efeito de linha embaixo no hover */
nav.menu-desktop ul li::after {
  content: ""; /* Para adicionar um elemento fictício */
  position: absolute;
  left: 50%;
  bottom: -5px; /* Distância do texto */
  width: 0; /* Começa com 0 de largura */
  height: 2px; /* Altura da linha */
  background: #0eacdb; /* Cor da linha */
  transition: width 0.3s ease, left 0.3s ease; /* Transição suave */
}

/* Efeito ao passar o mouse */
nav.menu-desktop ul li:hover::after {
  width: 100%; /* Expande a linha */
  left: 0; /* Alinha a linha à esquerda */
}

nav.menu-desktop ul {
  list-style-type: none; /* Remove marcadores */
}

/* TÍTULOS E TEXTOS */
h2.titulo {
  color: #000;
  font-size: 38px;
  text-align: center;
}

h2.titulo span {
  color: #0eacdb;
}

/* MEDIA QUERIES - RESPONSIVIDADE */

/* Ajustes para telas menores que 768px */
@media (max-width: 768px) {
  header > .interface {
    flex-direction: column;
    gap: 15px;
  }

  nav.menu-desktop ul li {
    display: block;
    text-align: center;
    padding: 10px 0;
  }

  .btn-contato button {
    width: 100%;
    max-width: 300px; /* Limita o tamanho máximo do botão */
  }
}

/* Ajustes para telas menores que 480px */
@media (max-width: 480px) {
  h1 {
    font-size: 6vh; /* Ajusta o tamanho do título para telas pequenas */
  }

  nav.menu-desktop ul li {
    padding: 5px 0;
  }

  .btn-contato button {
    padding: 12px 20px; /* Ajusta o padding para telas muito pequenas */
  }
}


</style>