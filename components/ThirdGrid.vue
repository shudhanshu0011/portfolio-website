<template>
<div>
  <section class="section-container section3">
    <div class="grid-container">

       
      <h2 class="points-title dev-title">Achievements
        <div class="title-line"></div>
      </h2>
            
      <div class="dev-point dev-point-1">
        <div class="point-title-container">
          <div class="circle-title"></div>
          <h4>2022</h4>
        </div>
        <p>Rank 2 among 50 teams participated in college level hackathon.</p>
      </div>

      <div class="icon dev-point-1-icon">
        <div class="icon-wrap dev-point-1-wrap">

        </div>
      </div>

      <div class="dev-point dev-point-2">
        <div class="point-title-container">
          <div class="circle-title"></div>
          <h4>2021</h4>
        </div>
        <p>Became 3 star rated programmer on Codechef.</p>
      </div>

      <div class="icon dev-point-2-icon">
        <div class="icon-wrap dev-point-2-wrap">
          <div class="desktop screen"></div>
        </div>
      </div>
      <div class="icon dev-point-2-icon">
        <div class="icon-wrap dev-point-2-wrap">
          <div class="desktop2 screen"></div>
        </div>
      </div>
      <div class="icon dev-point-2-icon">
        <div class="icon-wrap dev-point-2-wrap">
          <div class="desktop3 screen"></div>
        </div>
      </div>

      <div class="dev-point dev-point-3">
        <div class="point-title-container">
          <div class="circle-title"></div>
          <h4>Smart India Hackathon</h4>  
        </div>
        <p>Shortlisted team from our college for Smart India Hackathon.</p>
      </div>

      <div class="icon dev-point-3-icon">
        <div class="icon-wrap dev-point-3-wrap">
          <div class="line line1"></div>
          <div class="line line2"></div>
          <div class="line line3"></div>
          <div class="line line4"></div>
        </div>
      </div>


      <div class="icon dev-point-4-icon">
        <div class="icon-wrap dev-point-4-wrap">
          
        </div>
      </div>

    </div>
  </section>
</div>
</template>

<script>
export default {
  mounted(){
    $nuxt.$emit('third-grid-loaded')
  }
}
</script>