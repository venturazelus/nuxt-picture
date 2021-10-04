<template>
<div>
  <b-navbar sticky type="dark" variant="dark">
    <b-navbar-nav>
      <b-nav-item href="#">Home</b-nav-item>
      <b-nav-item href="#">Button2</b-nav-item>
      <b-nav-item href="#">Button3</b-nav-item>
    </b-navbar-nav>
  </b-navbar>

    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      background="#ababab"
      img-width="1024"
      img-height="480"
      class="ml-md-auto p-5 bg-info"
      style="text-shadow: 1px 1px 5px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide
        caption="First slide"
        text="Nulla vitae elit libero, a pharetra augue mollis interdum."
        img-src="https://picsum.photos/1024/480/?image=52"
      ></b-carousel-slide>

      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54">
        <h1>Hello world!</h1>
      </b-carousel-slide>

      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=58"></b-carousel-slide>

      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            width="1024"
            height="480"
            src="https://picsum.photos/1024/480/?image=55"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>

      <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
          a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
        </p>
      </b-carousel-slide>
    </b-carousel>

  <b-card>
    <b-row>
      <b-col>
      <b-card
        title="Card Title"
        img-src="https://picsum.photos/600/300/?image=25"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the bulk of the card's content.
        </b-card-text>

        <b-button href="#" variant="primary">Go somewhere</b-button>
      </b-card>
      </b-col>

      <b-col>
      <b-card
        title="Card Title"
        img-src="https://picsum.photos/600/300/?image=35"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the bulk of the card's content.
        </b-card-text>

        <b-button href="#" variant="primary">Go somewhere</b-button>
      </b-card>
      </b-col>

      <b-col>
      <b-card
        title="Card Title"
        img-src="https://picsum.photos/600/300/?image=15"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem;"
        class="mb-2"
      >
        <b-card-text>
          Some quick example text to build on the card title and make up the bulk of the card's content.
        </b-card-text>

        <b-button href="#" variant="primary">Go somewhere</b-button>
      </b-card>
      </b-col>
    </b-row>
  </b-card>

  <b-card no body>
    <b-tabs 
    justified
    active-nav-item-class="font-weight-bold text-uppercase text-danger"
    active-tab-class="font-weight-bold text-success"
    content-class="mt-3"
    >
      <b-tab  title="Picture 1">
        <b-card-img bottom src="https://picsum.photos/600/200/?image=64" alt="Image 64" ></b-card-img>
      </b-tab>

      <b-tab title="Picture 2">
        <b-card-img bottom src="https://picsum.photos/600/200/?image=65" alt="Image 65" ></b-card-img>
      </b-tab>

      <b-tab  title="Picture 3">
        <b-card-img bottom src="https://picsum.photos/600/200/?image=66" alt="Image 66"></b-card-img>
      </b-tab>

      <b-tab title="Picture 4">
       <b-card-img bottom src="https://picsum.photos/600/200/?image=67" alt="Image 67"></b-card-img>
      </b-tab>
      
    </b-tabs>
  </b-card>

</div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
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

<style scoped>
  .caraousel{
    margin: auto;
  }
  .card{
    margin: auto;
    display: inline;
  }
</style>