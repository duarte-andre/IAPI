<template>
  <div class="root-container"> <!-- Elemento raiz -->
    <header class="head">
      <Header />
    </header>
    <main>
      <section class="topo-site" id="topo-site">
        <!-- Exibindo a imagem kids.png da pasta assets -->
        <img :src="kidsImage" alt="Kids Image" class="main-image" />
        
        <div class="interface" style="margin-top: 90px;" id="txt-topo">
          <div class="flex">
            <div class="txt-topo" >
              <h1>SOBRE NÓS <span>.</span></h1>
              <br>
              <p style="font-size: 17px;  word-spacing: 4px; line-height: 1.5; text-align: justify ">
                O Instituto de Assistência e Proteção à Infância (IAPI) é uma organização dedicada à promoção do bem-estar e desenvolvimento de crianças e adolescentes em situação de vulnerabilidade.
                Nosso compromisso é garantir um ambiente seguro, acolhedor e propício para o crescimento saudável, oferecendo assistência social, educação e apoio integral.
                Trabalhamos para que cada jovem atendido tenha acesso a oportunidades que favoreçam seu futuro, contribuindo para uma sociedade mais justa e inclusiva.
              </p>
              <br>
              <br>
              <div class="bnt-ctt">
                <a href="#">
                  <button>Entre em Contato</button>
                </a>
              </div>
            </div>
            <div class="img-txt">
              <img
                src="https://scontent.fcgh51-1.fna.fbcdn.net/v/t1.6435-9/58622748_1016841341853555_2634545867217960960_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=0b6b33&_nc_eui2=AeHyvQinK8EpFKxufp_EqALVDw4QxxpJi4gPDhDHGkmLiBu0DsqTAWmyOY7h5YtjmdMU0b52-szexpozrP3qhK6f&_nc_ohc=8fyMSpH-H_kQ7kNvgGTMAp7&_nc_zt=23&_nc_ht=scontent.fcgh51-1.fna&_nc_gid=AEii2DAj44341WDRTyrYOiu&oh=00_AYCP8A5oT_OZlUaXgkKiK-qjWI8kZRqzRrTPpWhJDSK4Xg&oe=676718BA"
                alt="Imagem complementar"
              />
            </div>
          </div>
        </div>
      </section>
      <br>
      <br>

      <section class="especiliadades" id="especiliadades">
        <div class="interface">
          <h2 class="titulo" style="margin: 0px 35%; font-size: 35px;">NOSSOS <span style="color: #0eacdb;" >OBJETIVOS!</span></h2>
          <br>
          <div class="flex">
            <div class="especialidades-box">
              <i class="bi bi-card-text"></i>
              <h3>Valores</h3>
              <p style="text-align: justify;">
                Compromisso com ética, respeito, empatia e transparência, 
                promovendo o bem-estar e a dignidade de todas as crianças, 
                focando em inclusão e desenvolvimento integral.
              </p>
            </div>
            <!--especialidades-box-->

            <div class="especialidades-box">
              <i class="bi bi-arrow-through-heart"></i>
              <h3>Missão</h3>
              <p style="text-align: justify;">
                Promover a proteção e o desenvolvimento integral de crianças e adolescentes, oferecendo apoio social, 
                educacional e de saúde, garantindo um futuro mais seguro e digno.
              </p>
            </div>
            <!--especialidades-box-->

            <div class="especialidades-box" @click="abrirGoogleMaps">
              <i class="bi bi-pin-fill"></i>
              <h3>Visão</h3>
              <p style="text-align: justify;">
                Ser referência nacional na proteção à infância,
                 proporcionando oportunidades para transformar vidas 
                 e construir uma sociedade mais justa e inclusiva para crianças vulneráveis.
              </p>
            </div>
            <!--especialidades-box-->
          </div>
          <!--flex-->
          <br />
          <br />
          <div class="btn-social">
            <a href="https://www.facebook.com/iapi.org" target="_blank">
              <button><i class="bi bi-facebook"></i></button>
            </a>
          </div>
          <!--btn-social-->
        </div>
        <!--interface-->
      </section>
      <br>
      <br>
      <br>
      <section class="projeto">
        <div class="carrossel">
          <div class="carrossel-container" :style="{ transform: `translateX(-${currentSlide * 100}%)` }">
            <div class="carrossel-slide" v-for="(image, index) in carrosselImages" :key="index">
              <img :src="image.src" :alt="image.alt" class="carrossel-image" />
            </div>
          </div>
        </div>
      </section>
      <section class="desenvolvimento">
        <div class="cultura" id="cultura">
          <h1 style="font-size: 8vh;">Cultura e Esporte</h1>
          <br>

          <br>
          <p style="text-align: justify; font-size: 18px; word-spacing: 5px; line-height: 1.5;">
            Entre modalidades culturais e esportivas, ofertamos 9 oficinas para o público infanto-juvenil, de 6 a 17 anos. 
            As oficinas consistem em aulas de ukulele, ballet, canto, percussão, pintura, flauta, futebol, jiu-jitsu e basquete. 
            Essas aulas são acompanhadas por uma equipe pedagógica que analisa a desenvoltura dos alunos, bem como suas aptidões. 
            O aprendizado é colocado em prática de diversas maneiras, o que incluem os campeonatos e os eventos que promovemos, 
            fomentando a inserção dos alunos em diferentes espaços e ampliando o repertório sócio-cultural de cada um deles. 
            Nosso objetivo principal é possibilitar que esses locais se tornem redes interativas de inclusão e de promoção cultural vivas e dinâmicas, 
            apresentando aos nossos assistidos amplos horizontes e alto parâmetro de inspiração e conhecimento.
          </p>
        </div>
        <div></div>
        <br>
        <div class="projetos" style="margin-top: 40px;">
          <h1 style="font-size: 3.5vh;">Atividades Desenvolvidas para <br> Estimular a Criatividade</h1>
          <br>
          <p class="p1" style="text-align: justify; font-size: 18px; word-spacing: 4px; line-height: 1.5;">
            Aqui, as crianças recebem acompanhamento e auxílio de Educadoras Sociais nas tarefas escolares e participam de oficinas 
            pedagógicas como artes, música e esportes. Além disso, recebem alimentação completa e dispõem de atendimento especializado 
            de psicologia e psicopedagogia.
          </p>
          
        </div>
        <div class="img-proj" style="margin:0px 58%; margin-top: -270px;">
            <img width="300px" style="border-radius: 10px;"
                src="https://scontent.fgru11-1.fna.fbcdn.net/v/t1.6435-9/82792120_1229334757270878_6704409709576716288_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=0b6b33&_nc_eui2=AeEi2-HtYovRJEZTivy8kZs1ZT1TH6CKNlJlPVMfoIo2UqIfImmEodwnfRO2F_zjQTqmZmIS9Ff7B6z7q84gwbZO&_nc_ohc=0xNKSc7bDIsQ7kNvgE0N4cG&_nc_zt=23&_nc_ht=scontent.fgru11-1.fna&_nc_gid=A-2UVtgj8NorJ-TW4LSYbHp&oh=00_AYAJasl0ZD_TVgYKKkIIfQ128TowCLPpkZYiiMQvWmBrOA&oe=67673738"
                alt="Imagem complementar"
              />
        </div>
        <br>
        <div class="img-proj2" style="margin:0px 22%; margin-top: 100px; ">
            <img width="300px" style="border-radius: 10px;"
                src="https://scontent.fcgh28-1.fna.fbcdn.net/v/t1.6435-9/82500854_1216646585206362_4445687718575341568_n.png?_nc_cat=109&ccb=1-7&_nc_sid=0b6b33&_nc_eui2=AeFCl9C41StztM2EokkzDLJ01stPPkoCXT7Wy08-SgJdPru3PH1BCEbEIAjNqIkD4mTR27ICJLLsCrnlQf2g0-FW&_nc_ohc=XIlhOKoS6jAQ7kNvgEIwiSS&_nc_zt=23&_nc_ht=scontent.fcgh28-1.fna&_nc_gid=AjDIpWX1Cpm4n1CJYXORFd3&oh=00_AYAeDoLjmiW6W-x6k27IGvEALvaeIl_xCBMltRCnTsUYRQ&oe=67673752"
                alt="Imagem complementar"
              />
        </div>
        <div class="txt-final" style="margin-top: -310px; width: 25%; height: 20rem;">
          <h1 style="font-size: 3.5vh;">Desejamos aumentar o Número de assistidos.</h1>
          <br>
          <p class="p2" style="text-align: justify ; font-size: 18px; word-spacing: 4px; line-height: 1.5;">
            Buscamos ampliar nosso alcance e aumentar o número de assistidos na nossa ONG. Oferecemos apoio educacional, 
            oficinas de arte, música e esportes, além de alimentação nutritiva e atendimento psicológico. Cada contribuição 
            faz a diferença na vida das crianças que atendemos!
          </p>
          
        </div>
        

      </section>
     <br>
    <br>
    <br>

    </main>
    <footer class="footer">
      <Footer />
    </footer>
  </div>
</template>

<script>
import Header from '@/components/header.vue'; 
import Footer from '@/components/footer.vue';// Caminho para o Header
import kidsImage from '@/assets/kids.png'; // Imagem que não será usada no carrossel
import CoralImage from '@/assets/coral.png';
import KuleleImage from '@/assets/kulele.png';
import LutaImage from '@/assets/luta.png';
import PercussaoImage from '@/assets/percussao.png';

export default {
  components: {
    Header,
    Footer
  },

  
  data() {
    return {
      kidsImage,
      currentSlide: 0,
      carrosselImages: [
        { src: CoralImage, alt: 'Coral Image' },
        { src: KuleleImage, alt: 'Kulele Image' },
        { src: LutaImage, alt: 'Luta Image' },
        { src: PercussaoImage, alt: 'Percussão Image' },
      ],
    };
  },
  mounted() {
    // Troca automática das imagens a cada 4 segundos
    this.startCarrossel();
  },
  methods: {
    startCarrossel() {
      setInterval(() => {
        this.nextSlide();
      }, 4000); // Muda a cada 4 segundos (4000ms)
    },
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.carrosselImages.length;
    },
  },
};
</script>



<style scoped>
/* Adicionando fundo preto e ajustando a imagem principal */
.root-container {
  background-color: aliceblue;
}

.main-image {
  width: 100%;
  height: calc(100vh - 100px); /* Ocupa a altura da viewport, menos o header */
  object-fit: cover;
  object-position: center;
}

section.topo-site {
  position: relative;
  padding: 0px 0%;
  min-height: 80vh; /* Define uma altura mínima, mas permite que o conteúdo se expanda */
}

section.topo-site .flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
  flex-wrap: wrap; /* Permite que os itens quebrem de linha se necessário */
}

.topo-site h1 {
  color: black;
  font-size: 42px;
  line-height: 48px;
  margin-bottom: 20px;
}

.topo-site .txt-topo h1 span {
  color: #0eacdb;
}

.topo-site .txt-topo {
  color: black;
  margin: 20px 0;
  max-width: 600px;
  margin: 0px 8%;
}

.topo-site .img-txt img {
  width: 100%;
  max-width: 400px;
  animation: flutuar 2s ease-in-out infinite alternate;
  border-radius: 2%;
  margin: 0px -25%;
}

.bnt-ctt button {
  background-color: #0eacdb;
  color: black;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  font-size: 16px;
  border-radius: 4px;
}

@keyframes flutuar {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(10px);
  }
}

/* Adiciona um espaçamento entre as seções para evitar sobreposição */
section.especiliadades {
  padding: 40px 4%;
  margin-top: 40px; /* Adiciona espaço entre as seções */
}

section.especiliadades .flex {
  display: flex;
  gap: 60px;
}



.especiliadades .especialidades-box {
  color: black;
  padding: 40px;
  border-radius: 20px;
  margin-top: 45px;
  transition: 0.2s;
}

.especiliadades .especialidades-box:hover {
  transform: scale(1.05);
  box-shadow: 0 0 20px #0eacdb;
}

.especiliadades .especialidades-box i {
  font-size: 70px;
  color: #0eacdb;
}

.especiliadades .especialidades-box h3 {
  font-size: 28px;
  margin: 15px 0;
}

.btn-social button {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  border: none;
  background-color: #0eacdb;
  font-size: 22px;
  cursor: pointer;
  margin: 0 5px;
  transition: 0.2s;
}

.carrossel {
  position: relative;
  width: 100%;
  overflow: hidden;
  height: 550px; /* Ajuste conforme necessário */
}

.carrossel-container {
  display: flex;
  transition: transform 0.5s ease;
  width: 100%;
  height: 100%;
}

.carrossel-slide {
  min-width: 100%;
  height: 100%;
  box-sizing: border-box;
}

.carrossel-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.cultura {
  margin: 0px 15%;
  padding-top: 60px;
}

.projetos {
  margin: 0px 22%;
  padding-top: 70px;
}

.p1 {
  margin-right: 420px;
}

.txt-final {
  margin: 0px 46%; 
  

}

.p2 {
  margin-right: -50px;
  
}





</style>

