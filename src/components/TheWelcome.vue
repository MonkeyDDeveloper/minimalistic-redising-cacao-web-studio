<template>
  <main class="main-content">
    <img id="bigLogo" src="../assets/CacaoBigLogo.887ceb5.svg" alt="big_logo">
    <h1 v-motion-slide-top :delay="500" class="color-FFAB4D text-lg-start text-md-center text-center my-5">Cacao Web Studio</h1>
    <p v-motion-slide-left :delay="700" style="font-size: 4vw;" class="text-company-presentation fw-bolder text-lg-start text-md-center text-sm-center text-center">Tell us about the project you want to do</p>
    <p v-motion-slide-right :delay="900" style="font-size: 4vw;" class="text-company-presentation fw-bolder text-lg-start text-md-center text-sm-center text-center">We convert your ideas to web projects</p>
    <p v-motion-slide-bottom :delay="1000" style="font-size: 4vw;" class="color-FFAB4D text-company-presentation fw-bolder text-lg-start text-md-center text-sm-center text-center">Sure we can help you!</p>
    <div class="row justify-content-lg-end justify-content-center mt-4">
      <div class="col-auto">
        <button class="btn btn-warning fw-bolder">Contact us!</button>
      </div>
    </div>
    </main>
</template>
<script>
  export default {
    mounted() {
      document.title = "CacaoWebStudio - Home"
    }
  }
</script>
<style>
  .main-content {
    position: relative;
  }
  #bigLogo {
    position: fixed;
    width: 60%;
    height: auto;
    right: 0;
    top: 0;
    z-index: -99;
    opacity: 0.1;
  }
  @media (width < 990px) {
    #bigLogo {
      width: 100%;
      top: center;
      right: center;
    }
    .main-content {
      display: flex;
      flex-direction: column;
    }
  }
  @media (width < 550px) {
    #bigLogo {
      width: 150%;
      top: 15%;
      right: -8%;
    }
  }
  html[data-bs-theme=light] #bigLogo {
    opacity: 0.3;
  }
  html[data-bs-theme=light] .text-company-presentation {
    text-shadow: 1px 1px 2px#FFAB4D;
  }
  .color-FFAB4D {
    color: #FFAB4D;
  }
  .bg-color-FFAB4D {
    background-color: #FFAB4D;
  }
</style>
