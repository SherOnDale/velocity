<template>
  <div class="full-container">
    <Flickity ref="flickity" :options="flickityOptions" class="slideshow">
      <div class="carousel-cell"></div>
      <div class="carousel-cell"></div>
      <div class="carousel-cell"></div>
      <div class="carousel-cell"></div>
    </Flickity>
    <div class="right-container">
      <div class="countdown">
        <div class="title">Lorem ipsum dolor sit amet.</div>
        <div
          class="subtitle"
        >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolore maiores fugit corrupti facilis ab neque, atque molestiae veniam similique expedita!</div>
        <div class="cta">call to action</div>
      </div>
      <div class="hero">
        <div class="title">Lorem ipsum dolor sit amet.</div>
        <div
          class="subtitle"
        >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolore maiores fugit corrupti facilis ab neque, atque molestiae veniam similique expedita!</div>
        <div class="cta">call to action</div>
      </div>
    </div>
    <sponsors/>
  </div>
</template>

<script>
import sponsors from "../components/sponsors";

export default {
  data() {
    return {
      flickityOptions: {
        intialIndex: 0,
        prevNextButtons: true,
        pageDots: true,
        wrapAround: true,
        autoPlay: true
      }
    };
  },
  components: {
    sponsors
  }
};
</script>

<style>
.right-container {
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 50vh;
}

.full-container {
  height: 100vh;
  width: 100vw;
  background-color: rgba(49, 84, 49, 0.7);
  display: flex;
  justify-content: stretch;
  padding-top: 8rem;
}

.slideshow {
  padding: 0 2rem;
  border-bottom: 2rem solid rgba(0, 0, 0, 0);
  height: 50vh;
  width: 100%;
}

.carousel-cell {
  width: 100%;
  height: 50vh;
  background-image: url(/bg1.jpg);
  background-position: center;
  background-size: cover;
}

.countdown {
  margin-bottom: 2rem;
}

.hero,
.countdown {
  background-color: rgba(0, 0, 0, 0.6);
  width: 35vw;
  padding: 2rem;
}

.hero .title,
.countdown .title {
  font-family: Staatliches, cursive;
  font-size: 3rem;
  color: #3e377c;
}
.hero .subtitle,
.countdown .subtitle {
  margin-top: 1rem;
  font-family: Dosis, sans-serif;
  font-size: 1.2rem;
  line-height: 1.5rem;
  letter-spacing: 0.1rem;
}

.hero .cta,
.countdown .cta {
  text-transform: uppercase;
  font-family: Staatliches, cursive;
  font-size: 1.2rem;
  font-weight: 800;
  margin-top: 3rem;
  color: rgb(62, 55, 124);
  letter-spacing: 0.1rem;
  border-bottom: 1px solid #3e377c;
  width: 7.8rem;
  padding-bottom: 0.5rem;
}
</style>
