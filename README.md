# Indicoproject
Document Gallery
<!DOCTYPE html>
<html>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  font-family: Verdana, sans-serif;
  margin: 10;
}

* {
  box-sizing: border-box;
}

.row > .column {
  padding: 2 -3 14px;
}

.row:after {
  content: "";
  display: table;
  clear: both;
}

.column {
  float: left;
  width: 30%;
}

/* The Modal (background) */
.modal {
  display: none;
  position: fixed;
  z-index: 1;
  padding-top: 70px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: lightgray;
}

/* Modal Content */
.modal-content { 
  position: relative;
  background-color: #808080;
  margin: auto;
  padding: 0;
  width: 80%;
  max-width: 900px;
}

/* The Close Button */
.close {
  color: black;
  position: absolute;
  top: 10px;
  right: 25px;
  font-size: 35px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: #999;
  text-decoration: none;
  cursor: pointer;
}

.mySlides {
  display: none;
}

.cursor {
  cursor: pointer;
}

/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  margin-top: -50px;
  color: white;
  font-weight: bold;
  font-size: 20px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
  -webkit-user-select: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

img {
  margin-bottom: 4px;
}

.caption-container {
  text-align: center;
  background-color: white;
  padding: 2px 16px;
  color: black;
}

.demo {
  opacity: 0.8;
}

.active,
.demo:hover {
  opacity: 2;
}

img.hover-shadow {
  transition: 0.3s;
}

.hover-shadow:hover {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
</style>
<body>

<h2 style="text-align:center"></h2>

<div class="row">
  <div class="column">
    <img src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/10/2.-carta-rei-do-congo.jpg" style="width:85%" onclick="openModal();currentSlide(1)" class="hover-shadow cursor">
  </div>
  <div class="column">
    <img src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/07/Solicitacao-de-alvara.jpg" style="width:85%" onclick="openModal();currentSlide(2)" class="hover-shadow cursor">
  </div>
  <div class="column">
    <img src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/07/carta-em-marata.jpg" style="width:85%" onclick="openModal();currentSlide(3)" class="hover-shadow cursor">
  </div>
</div>

<div id="myModal" class="modal">
  <span class="close cursor" onclick="closeModal()">&times;</span>
  <div class="modal-content">

    <div class="mySlides">
      <div class="numbertext">1 / 3</div>
      <img src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/10/2.-carta-rei-do-congo.jpg" style="width:100%">
    </div>

    <div class="mySlides">
      <div class="numbertext">2 / 3</div>
      <img src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/07/Solicitacao-de-alvara.jpg" style="width:100%">
    </div>

    <div class="mySlides">
      <div class="numbertext">3 / 3</div>
      <img src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/07/carta-em-marata.jpg" style="width:100%">
    </div>
    
    <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
    <a class="next" onclick="plusSlides(1)">&#10095;</a>

    <div class="caption-container">
      <p id="caption"></p>
    </div>


    <div class="column">
      <img class="demo cursor" src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/10/2.-carta-rei-do-congo.jpg" style="width:0%" onclick="currentSlide(1)" alt ="Letter from the King of Congo to the Governor of Angola. Luanda, 1815. AHU, Angola, cx. 130, doc. 113. 1815 (20 de dezembro) - São Paulo da Assumpção de Luanda.Carta do governador de Angola enviando uma carta escrita pelo rei do Congo, D. Garcia V. A carta dá conta do seu casamento com a rainha D. Isabel e do sepultamento na sé de São Salvador de sua mãe, cerimónias que tinham sido possíveis graças à presença dos padres missionários enviados pelo governador de Angola. Neste sentido, relata como o Pe. Fr. Luís Maria de Assis, prefeito de Santo António em Luanda, batizara muitos habitantes locais, antes de ter regressado para a costa deixando saudades. O rei volta a pedir que se enviem eclesiásticos para o Congo, escrevendo: “Ah, meu irmam Rei como eu, mas mais felix por ter muitos sacerdotes”. Refere o costume anterior de os missionários que passavam uma temporada no Congo serem depois nomeados como embaixadores do reino em Portugal ou Roma.">
    </div>
    <div class="column">
      <img class="demo cursor" src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/07/Solicitacao-de-alvara.jpg" style="width:0%" onclick="currentSlide(2)" alt="Request for “assimilation permit”. Lourenço Marques (Maputo), 1938. AHM, Moçambique, Cx. 1623, 1938 (18 de Julho) - Lourenço Marques. Carta de Antonio José de Carvalho, natural de Inhambane e empregado da W.N.L.A., para o Diretor da Repartição Central dos Negócios Indígenas, solicitando segunda via de um “alvará de isenção (ou assimilação)”.">
    </div>
    <div class="column">
      <img class="demo cursor" src="http://indico.ics.ulisboa.pt/wp-content/uploads/2020/07/carta-em-marata.jpg" style="width:0%" onclick="currentSlide(3)" alt="Letter written in Marathi by Gonda Rao. Goa, 1711, AHU, Índia, cx. 101, 1711 (14 de Janeiro). Informação sobre o ofício que pede Gonda Rao de capitão mor dos mais dessais. Afirma que os “reis antiguissimos” tinham feito mercê do sardessaiado das terras de Pondá e de todas as suas tenças e pertenças aos ascendentes de Gondá Rao, que reclamava a mercê de capitão mor dos mais dessais, para serem passadas aos seus descendentes. Estes descendentes eram sempre encabeçados pelo primogénito, da casa tendo a primogenitura passado de seu pai Dulba Naique para o seu irmão Nagogi Naique. Porém, ao longo do tempo as terras tinham sido tomadas por vários potentados, apoiados ocasionalmente por ramos colaterais da família dos dessais, os quais se apoderaram das ditas tenças e pertenças pagando valores irrisórios a Nagogi Naique e Gonda Rao, que habitavam em Goa. Pede por isso para ser nomeado capitão mor dos dessais, devendo os restantes ficar em obediência a si. É acompanhado por uma versão em marata.">
    </div>
</div>

<script>
function openModal() {
  document.getElementById("myModal").style.display = "block";
}

function closeModal() {
  document.getElementById("myModal").style.display = "none";
}

var slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("demo");
  var captionText = document.getElementById("caption");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
  captionText.innerHTML = dots[slideIndex-1].alt;
}
</script>
    
</body>
</html>
