<template>
<div>
  <section class="section-container section">
    <div class="loading-bg">
      <!-- <div class="loading-text">33%</div> -->
    </div>

    <div class="grid-container">
    

    <div class="name">
      <h1>
        <span class="name-letter-0">[</span>
        <span class="name-letter-1">S</span>
        <span class="name-letter-2">h</span>
        <span class="name-letter-3">u</span>
        <span class="name-letter-4">d</span>
        <span class="name-letter-5">h</span>
        <span class="name-letter-6">a</span>
        <span class="name-letter-7">n</span>
        <span class="name-letter-8">s</span>
        <span class="name-letter-9">h</span>
        <span class="name-letter-10">u</span>
        <span>&nbsp;</span>
        <span class="name-letter-11">R</span>
        <span class="name-letter-12">a</span>
        <span class="name-letter-13">n</span>
        <span class="name-letter-14">j</span>
        <span class="name-letter-15">a</span>
        <span class="name-letter-16">n</span>
        <span class="name-letter-17">]</span>
      </h1>
    </div>

    <div class="services opacity-fade-in translate-in">
      <p class="service service-0"></></p>
      <p class="service service-1">2024 Grad</p>
      <p class="service service-2">Web Developer</p>
      <p class="service service-3">Codechef 3*</p>
      <p class="service service-4">C++ | JS | React</p>
      <!-- <p class="service service-5">Design Research</p> -->
      <div class="available opacity-fade-in translate-in">
      <Available/>
      </div>
    </div>

    <ProjectsList class="projects" />
    </div>
  </section>
</div>
</template>

<script>
import { gsap } from "gsap"
export default {
    mounted() {
    const tlLoad = gsap.timeline({})

    tlLoad
    .to(".loading-bg", { yPercent: -100, duration: 5, ease: "Expo.easeInOut" })
    .to(".loading-bg", { xPercent: 1000, duration: 0, ease: "none" })
    .to('.name h1',{fontSize:"8.3vw", duration:2, ease:'Power4.easeInOut',},"-=1")
    // onComplete:function(){
    //   document.querySelector('.name h1').classList.add('name-hover-effect')
    // }
    .from(".opacity-fade-in", { opacity: 0, duration: 4, ease: "Power4.easeOut" })
    .from(".translate-in", { yPercent: 200, duration: 3, ease: "Power4.easeOut" }, "<")
    
    // .from(".translate-in-slow", { yPercent: 100, opacity: 0, duration: 4, ease: "Power4.easeOut"}, "<")
    .from(".translate-in-left", { xPercent: -100, duration: 2, ease: "Power4.easeOut" }, "<+=1")

    setTimeout(()=>{
      const projects = document.querySelectorAll('.project')
      document.querySelector(`.projects`).style.display = "flex"
      let counter = 0;
      for (let i = 0; i < projects.length; i++) {
        tlLoad.from(`.project-${i}`,{ yPercent: 500, ease: 'Power4.easeOut', duration: 2, delay: counter * 0.2,}, '<' )
        counter += 0.5
      }},2000)

    }
}
</script>

<style scoped lang="scss">

  section{
    background-color: white;
  }

  #awwwards{
    @media screen and (min-width: 320px) {
      display:none;
    }
    @media screen and (min-width: 720px) {
      display:inline;
    }
  }

  .loading-bg {
    width:120vw;
    height: 120vh;
    background-color:#000;
    position:fixed;
    z-index: 100;
    display:flex;
    flex-direction:column-reverse;
    margin-left: -$margin;
    margin-top: -$margin;
    .loading-text{
      color:white;
      font-size:5rem;
      align-self: flex-end;
    }
  }
</style>