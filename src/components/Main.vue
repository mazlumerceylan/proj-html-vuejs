<template>
<div class="jumbotron">
  <div class="left-section">
    <h1>Start Investing in Yourself</h1>
    <p>
      With over 1200 courses in 18 subjects, you're guaranteed to find something that's right for you.
    </p>
    <button type="button">Join for Free</button>
  </div>
  <div class="right-section">
    <img class="base-image" src="src/assets/img/base.png" alt="Immagine base">
    <img class="overlay-book-1" src="src/assets/img/book1.png" alt="Immagine 1">
    <img class="overlay-book-2" src="src/assets/img/book2.png" alt="Immagine 2">
    <img class="overlay-chat" src="src/assets/img/bubblespeech.png" alt="Immagine 3">
    <img class="overlay-glass" src="src/assets/img/magnifier.png" alt="Immagine 4">
  </div>
</div>

<div class="card-container">
  <div class="card-icon">
    <i class="fa-solid fa-earth-americas"></i>
    <h2>Worldwide Trends</h2>
    <p>Our services and collections adhere to cutting-edge solutions in the design world.
    </p>
  </div>

  <div class="card-icon">
    <i class="fa-solid fa-display"></i>
    <h2>Complex Online Education</h2>
    <p>We have everything for effective learning and delivery of assignments by students.
    </p>
  </div>

  <div class="card-icon">
    <i class="fa-regular fa-calendar"></i>
    <h2>Brand certificate</h2>
    <p>After completing the course, you will receive a certificate confirming your knowledge.</p>
  </div>
</div>


<div class="courses-category">
  <div class="card-ctg big">
    <img class="photo-courses-big" src="src/assets/img/cat_1-770x375.jpg" alt="image">
    <p>Software Developer</p>
  </div>

  <div class="card-ctg small">
    <div>
      <img class="photo-courses-small" src="src/assets/img/cat_2-370x155.jpg" alt="image">
      <p>Art</p>
    </div>
    <div>
      <img class="photo-courses-need-fix" src="src/assets/img/cat_3-370x155.jpg" alt="image">
      <p>Material Design</p>
    </div>
  </div>
</div>
<div class="card--course-bottom">
  <div>
    <img src="src/assets/img/cat_5-370x155.jpg" alt="image">
    <p>Music</p>
  </div>

  <div>
    <img src="src/assets/img/cat_4-370x155.jpg" alt="image">
    <p>Exercise</p>
  </div>

  <div>
    <img src="src/assets/img/cat_6-370x155.jpg" alt="image">
    <p>Photograohy</p>
  </div>
</div>

</template>

<script>
import { mapState } from 'vuex'

export default {

}
</script>

<style>

@import '../scss/Main.scss';

</style>