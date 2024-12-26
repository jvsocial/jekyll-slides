---
layout: default
title: Presentation
---

<div id="slides-container">
  <div class="slide" id="slide-1">
    <h1>Slide 1</h1>
    <p>This is the content of the first slide.</p>
  </div>
  <div class="slide" id="slide-2">
    <h1>Slide 2</h1>
    <p>This is the content of the second slide.</p>
  </div>
  <div class="slide" id="slide-3">
    <h1>Slide 3</h1>
    <p>This is the content of the third slide.</p>
  </div>
</div>

<!-- Navigation Buttons -->
<div id="nav-buttons">
  <button onclick="prevSlide()">Previous</button>
  <button onclick="nextSlide()">Next</button>
</div>

<script>
  let currentSlide = 0;
  const slides = document.querySelectorAll('.slide');
  const totalSlides = slides.length;

  function showSlide(index) {
    // Hide all slides
    slides.forEach(slide => slide.style.display = 'none');
    
    // Show the current slide
    slides[index].style.display = 'block';
  }

  function nextSlide() {
    if (currentSlide < totalSlides - 1) {
      currentSlide++;
    } else {
      currentSlide = 0; // Loop back to the first slide
    }
    showSlide(currentSlide);
  }

  function prevSlide() {
    if (currentSlide > 0) {
      currentSlide--;
    } else {
      currentSlide = totalSlides - 1; // Loop to the last slide
    }
    showSlide(currentSlide);
  }

  // Show the first slide initially
  showSlide(currentSlide);
</script>
