<template>
<div class="Site">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      fade
      controls
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=51"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=52"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=53"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=55"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=56"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=57"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=59"></b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=60"></b-carousel-slide>
    </b-carousel>

 <footer class="footer">
      <b-row>
        <b-col class="text-right">
          <b-card-img width="100" height="100" right src="img/109919.jpg"/>
        </b-col>
        <b-col class="text-left">
          <b>venturazelus.com</b>
          <br>Jl. Kilimanjaro 25, Batu, Jawa Timur, Indonesia
          <br> Everyday 08.00-21.00
        </b-col>     
      </b-row>
  </footer>

</div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null,
      }
    },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
    }
  }
</script>

<style>
  .caraousel{
  margin: auto;
  }
  .footer{
  width: 99%;
  position: absolute;
  padding: auto;
  bottom: 0px; 
  font-size: 20px;
  color: black;  
  text-align: center;
  }
</style>