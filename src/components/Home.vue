<template>
  <div class="home">
   <b-navbar variant="success">
     <b-navbar-brand href="#">GLAM House</b-navbar-brand>
      <b-navbar-nav>
        <b-nav-item>SHOP</b-nav-item>
        <b-nav-item>BLOG</b-nav-item>
        <b-nav-item>GALLERY</b-nav-item>
        <b-nav-item>SERVICES</b-nav-item>
        <b-nav-item>PRODUCTS</b-nav-item>
      </b-navbar-nav>
      <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form>
   </b-navbar>

   <div>
     <b-carousel id="carousel-fade" style="text-shadow: 0px 0px 2px #000" fade indicators>
     <b-carousel-slide>
       <template v-slot:img>
         <img caption="Second Slide" src="../assets/first.jpg" class="carousel">
       </template>
     </b-carousel-slide>
     <b-carousel-slide>
       <template v-slot:img>
         <img caption="Second Slide" src="../assets/second.jpg" class="carousel">
       </template>
     </b-carousel-slide>
     <b-carousel-slide>
       <template v-slot:img>
         <img caption="Second Slide" src="../assets/third.jpg" class="carousel">
       </template>
     </b-carousel-slide>
    </b-carousel>
    </div>
    <section>
      <h4>Product Merchants</h4>
      <div class="products">
        <div class="merchants">
        <img src="../assets/byredo.png" class="image">
        <div class="details">
          <h5>Perfume</h5>
          <p>Byredo</p>
          <p>$39</p>
          <button class="button" v-on:click="booked"> Add to Cart</button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/midnight.jpeg" class="image">
        <div class="details">
          <h5>Perfume</h5>
          <p>Midnight</p>
          <p>$19</p>
          <button class="button" v-on:click="booked"> Add to Cart</button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/Miss-Dior.jpg" class="image">
        <div class="details">
           <h5>Perfume</h5>
           <p>Miss Dior</p>
           <p>$49</p>
           <button class="button" v-on:click="booked"> Add to Cart</button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/pink.jpeg" class="image">
        <div class="details">
          <h5>Perfume</h5>
          <p>Pink</p>
          <p>$29</p>
          <button class="button" v-on:click="booked"> Add to Cart</button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/villain.jpg" class="image">
        <div class="details">
          <h5>Perfume</h5>
          <p>Villain Black</p>
          <p>$69</p>
          <button class="button" v-on:click="booked"> Add to Cart</button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/white.jpg" class="image">
        <div class="details">
           <h5>Perfume</h5>
           <p>White</p>
           <p>$39</p>
           <button class="button" v-on:click="booked"> Add to Cart</button>
        </div>
      </div>
      </div>
    </section>
    <section>
      <h4>Service Merchants</h4>
      <div class="services">
        <div class="merchants">
        <img src="../assets/it-studios.jpeg" class="image">
        <div class="details">
          <h5>Make up artist</h5>
          <p>It Studios</p>
          <p>$50 per session</p>
          <b-button class="button" v-b-modal.modal-1> Book Now</b-button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/kld.jpg" class="image">
        <div class="details">
          <h5>Make up artist</h5>
          <p>King lade Dammy</p>
          <p>$30 per session</p>
          <b-button class="button" v-b-modal.modal-1>Book Now</b-button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/lush.jpeg" class="image">
        <div class="details">
          <h5>Make up artist</h5>
          <p>Lush beauty pro</p>
          <p>$40 per session</p>
          <b-button class="button" v-b-modal.modal-1> Book Now</b-button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/rheevo.jpeg" class="image">
        <div class="details">
          <h5>Make up artist</h5>
          <p>House of Rheevo</p>
          <p>$70 per session</p>
        <b-button class="button" v-b-modal.modal-1>Book Now</b-button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/zamore.jpg" class="image">
        <div class="details">
          <h5>Make up artist</h5>
          <p>Glam by zamore</p>
          <p>$20 per session</p>
          <b-button class="button" v-b-modal.modal-1>Book Now</b-button>
        </div>
      </div>
       <div class="merchants">
        <img src="../assets/amaks.jpg" class="image">
        <div class="details">
          <h5>Make up artist</h5>
          <p>Renemaks</p>
          <p>$25 per session</p>
          <b-button class="button" v-b-modal.modal-1> Book Now</b-button>
        </div>
      </div>
      </div>

      <b-modal id="modal-1" title=" Select Event">
        <div>
          <b-form-group label="Event">
            <b-form-radio v-model="selected" name="some-radios" value="Wedding">Wedding</b-form-radio>
            <b-form-radio v-model="selected" name="some-radios" value="Birthday">Birthday</b-form-radio>
            <b-form-radio v-model="selected" name="some-radios" value="Others">Others</b-form-radio>
          </b-form-group>

          <div class="mt-3">Selected: <strong>{{ selected }}</strong></div>
          </div>
      </b-modal>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Home',
  methods: {
    booked: function(){
      alert('Added to cart!')
    }
  },
  data() {
      return {
        selected: ''
      }
    }

}
</script>

<style scoped>
.carousel{
  width: 100%;
  height: 80vh;
}
.navbar{
  display: flex;
  justify-content: space-between;
}
h4{
  text-align: center;
  margin-top: 5%;
}
.products, .services{
  display: flex;
  flex-wrap: wrap;
  margin: 5% 0 0 10%;
}
.merchants{
  width: 30%;
  text-align: center;
  margin-bottom: 5%;
}
.image{
  width: 20vw;
  height: 35vh;
}
.details{
  padding-top: 1em;
}
.button{
  background: #000000;
  color: #ffffff;
  width: 15vw;
  height: 6vh;
  border: none;
  border-radius: 5px;
}
</style>
