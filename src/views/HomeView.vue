<script>
  import { Swiper, SwiperSlide } from 'swiper/vue';
  import { Autoplay, Pagination, Navigation } from 'swiper/modules';

  import 'swiper/css';
  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
        modules: [Autoplay, Pagination, Navigation],
      };
    },
  };
</script>
<template>
  <header class="header-sticky header-absolute">
      <nav class="navbar navbar-expand-xl navbar-fixed-top">
        <div class="container">
          <a class="navbar-brand me-0 d-flex" href="/">
            <img class="light-mode-item navbar-brand-item me-2" src="/src/assets/logo.png" width="70" height="70" alt="logo">
            <img class="dark-mode-item navbar-brand-item me-2" src="/src/assets/logo.png" alt="logo">
          </a>

          <div class="navbar-collapse collapse" id="navbarCollapse">
              <ul class="navbar-nav navbar-nav-scroll mx-auto">
                  <li class="nav-item">
                      <a class="nav-link" href="/"> Home</a>
                  </li>
                  <li class="nav-item">
                      <a class="nav-link" href="#">Skills</a>
                  </li>
                  <li class="nav-item">
                      <a class="nav-link" href="#">Portfolio</a>
                  </li>
                  <li class="nav-item"> <a class="nav-link" href="">Contact</a> </li>
              </ul>
          </div>

          <ul class="nav align-items-center dropdown-hover ms-sm-2">
              <li class="nav-item d-none d-sm-block me-5">
                  <button class="btn btn-sm btn-primary mb-0">Download CV</button>
              </li>
              <li class="nav-item dropdown dropdown-animation">
                  <button class="btn btn-link mb-0 px-2 lh-1" id="bd-theme"
                  type="button"
                  aria-expanded="false"
                  data-bs-toggle="dropdown"
                  data-bs-display="static">
                  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20"  class="bi bi-circle-half theme-icon-active fill-mode fa-fw" viewBox="0 0 16 16">
                      <path d="M8 15A7 7 0 1 0 8 1v14zm0 1A8 8 0 1 1 8 0a8 8 0 0 1 0 16z"/>
                      <use href="#"></use>
                  </svg>
                  </button>

                  <ul class="dropdown-menu min-w-auto dropdown-menu-end" aria-labelledby="bd-theme">
                      <li class="mb-1">
                          <button type="button" class="dropdown-item d-flex align-items-center" data-bs-theme-value="light">
                              <svg width="16" height="16" fill="currentColor" class="bi bi-brightness-high-fill fa-fw mode-switch me-1" viewBox="0 0 16 16">
                                  <path d="M12 8a4 4 0 1 1-8 0 4 4 0 0 1 8 0zM8 0a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 0zm0 13a.5.5 0 0 1 .5.5v2a.5.5 0 0 1-1 0v-2A.5.5 0 0 1 8 13zm8-5a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2a.5.5 0 0 1 .5.5zM3 8a.5.5 0 0 1-.5.5h-2a.5.5 0 0 1 0-1h2A.5.5 0 0 1 3 8zm10.657-5.657a.5.5 0 0 1 0 .707l-1.414 1.415a.5.5 0 1 1-.707-.708l1.414-1.414a.5.5 0 0 1 .707 0zm-9.193 9.193a.5.5 0 0 1 0 .707L3.05 13.657a.5.5 0 0 1-.707-.707l1.414-1.414a.5.5 0 0 1 .707 0zm9.193 2.121a.5.5 0 0 1-.707 0l-1.414-1.414a.5.5 0 0 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .707zM4.464 4.465a.5.5 0 0 1-.707 0L2.343 3.05a.5.5 0 1 1 .707-.707l1.414 1.414a.5.5 0 0 1 0 .708z"/>
                                  <use href="#"></use>
                              </svg>Light
                          </button>
                      </li>
                      <li class="mb-1">
                          <button type="button" class="dropdown-item d-flex align-items-center" data-bs-theme-value="dark">
                              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-moon-stars-fill fa-fw mode-switch me-1" viewBox="0 0 16 16">
                                  <path d="M6 .278a.768.768 0 0 1 .08.858 7.208 7.208 0 0 0-.878 3.46c0 4.021 3.278 7.277 7.318 7.277.527 0 1.04-.055 1.533-.16a.787.787 0 0 1 .81.316.733.733 0 0 1-.031.893A8.349 8.349 0 0 1 8.344 16C3.734 16 0 12.286 0 7.71 0 4.266 2.114 1.312 5.124.06A.752.752 0 0 1 6 .278z"/>
                                  <path d="M10.794 3.148a.217.217 0 0 1 .412 0l.387 1.162c.173.518.579.924 1.097 1.097l1.162.387a.217.217 0 0 1 0 .412l-1.162.387a1.734 1.734 0 0 0-1.097 1.097l-.387 1.162a.217.217 0 0 1-.412 0l-.387-1.162A1.734 1.734 0 0 0 9.31 6.593l-1.162-.387a.217.217 0 0 1 0-.412l1.162-.387a1.734 1.734 0 0 0 1.097-1.097l.387-1.162zM13.863.099a.145.145 0 0 1 .274 0l.258.774c.115.346.386.617.732.732l.774.258a.145.145 0 0 1 0 .274l-.774.258a1.156 1.156 0 0 0-.732.732l-.258.774a.145.145 0 0 1-.274 0l-.258-.774a1.156 1.156 0 0 0-.732-.732l-.774-.258a.145.145 0 0 1 0-.274l.774-.258c.346-.115.617-.386.732-.732L13.863.1z"/>
                                  <use href="#"></use>
                              </svg>Dark
                          </button>
                      </li>
                      <li>
                          <button type="button" class="dropdown-item d-flex align-items-center active" data-bs-theme-value="auto">
                              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-circle-half fa-fw mode-switch me-1" viewBox="0 0 16 16">
                                  <path d="M8 15A7 7 0 1 0 8 1v14zm0 1A8 8 0 1 1 8 0a8 8 0 0 1 0 16z"/>
                                  <use href="#"></use>
                              </svg>Auto
                          </button>
                      </li>
                  </ul>
              </li>
              <!-- Responsive navbar toggler -->
              <li class="nav-item">
                  <button class="navbar-toggler ms-sm-3 p-2" type="button" data-bs-toggle="collapse" data-bs-target="#navbarCollapse" aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
                      <span class="navbar-toggler-animation">
                          <span></span>
                          <span></span>
                          <span></span>
                      </span>
                  </button>
              </li>	
          </ul>
        </div>
      </nav>
  </header>
  <main>
    <section class="position-relative overflow-hidden pt-xl-9">
      <div class="position-absolute top-0 start-0 ms-n7 d-none d-xl-block">
          <img src="/decoration-pattern.svg" alt="">
      </div>
      <figure class="position-absolute top-0 end-0 me-n4 mt-n7 d-none d-xl-block">
              <svg class="fill-mode opacity-1" width="775px" height="834px" viewBox="0 0 775 834" style="enable-background:new 0 0 775 834;" xml:space="preserve">
                  <path d="M486.1,564.4c-3.6,2.5-7.4,4.8-11.3,6.4c-12,5.5-25.7,7.9-42.2,7.4c-30.6-1.1-65.6-12.5-102.8-24.4 c-50.7-16.2-103.3-33.4-152.5-27c-56.1,7.2-97.9,44.4-128,114l-0.4-0.2c67.5-156.1,181-119.5,281.1-87.1c37,12,72,23.2,102.5,24.3 c34.3,1.2,58.1-10.7,74.9-37.4C530.1,505,547.1,466,565,425.1C619.4,301,675.6,172.7,892.1,141.3l0.1,0.4 c-216.2,31.4-272.5,159.5-326.8,283.5c-18.1,41.1-35,79.7-57.7,115.6C501.6,550.7,494.5,558.5,486.1,564.4z"/>
                  <path d="M500.9,551.4c-43.7,31-103,15.8-165.5-0.2c-49.9-12.7-101.5-25.8-148.7-16.7c-53.3,10.5-93.2,49-121.6,118 l-0.5-0.1c15.3-37.1,33.3-64.7,55.1-84.7c19.5-17.7,41.3-28.6,66.7-33.7c47.4-9.2,99,3.9,148.9,16.6 c70.4,17.9,137.1,34.9,181.3-14.4c35.7-39.9,57.3-91.7,80.2-146.7c23.8-56.7,48.2-115.5,90.2-163.6c22.7-25.9,48.4-46.4,78.4-62.4 c33.9-18.1,72.2-30.3,117.1-37.1l0.1,0.4C695,155.3,645.2,274.5,597.1,389.7c-22.9,55-44.5,106.8-80.4,146.8 C512.3,542.4,506.6,547.3,500.9,551.4z"/>
                  <path d="M521.3,536.4c-21.9,15.5-48.4,23.4-80.8,23.8c-31.2,0.5-65.1-5.8-97.9-11.9c-49.3-9.2-100.2-18.7-145.7-6.5 c-51.1,13.7-88.9,53.7-116,122.6l-0.6-0.2c60.5-154.1,163.3-135,262.6-116.5c68.1,12.7,132.6,24.6,183.6-15.8 c48.1-38.2,71.1-100.6,95.6-166.5c20.3-55,41.4-111.6,78.3-158.1c20-25.1,42.7-44.9,69.2-60.5c30.1-17.5,64.2-29.1,104.3-35.4 l0.2,0.6c-167.2,26.3-210,141.9-251.4,253.5C598.3,431.5,575,493.8,527,532.2C525.1,533.8,523.2,535.1,521.3,536.4z"/>
                  <path d="M548.9,520.3c-4,2.9-8.2,5.6-12.6,8c-56.6,31.5-120.9,23.8-183,16.6c-51.7-6-100.4-11.8-144.6,3.2 c-49.9,16.9-85.5,57.7-111.3,128.2l-0.6-0.2c13.7-37.3,30.1-66,49.9-87.8c17.8-19.4,37.9-32.8,61.8-40.9 c44.3-15,93.1-9.3,144.9-3.2c62.1,7.2,126.3,14.8,182.8-16.6c59.6-33.2,82-104.7,105.9-180.4c17.1-54.3,34.7-110.5,67.2-156.6 c36.7-52,87.8-82.8,155.7-94l0.2,0.6c-151.9,25-187.8,139.3-222.3,250C620.4,417.6,599.4,484.5,548.9,520.3z"/>
                  <path d="M573.5,509.5c-8.2,5.8-17.4,10.7-27.7,14.6c-59.3,22-119.1,18.8-176.8,15.8c-53.2-2.8-103.3-5.3-147.1,12.5 C172.6,572.3,138.1,615.5,113,688l-0.5-0.1c25.1-72.7,59.6-115.9,108.9-136c44-18,94.2-15.3,147.6-12.6 c57.7,3,117.4,6.1,176.6-15.9c70.7-26.2,91.1-106.3,112.8-191.4c13.9-54.5,28.3-111,56.7-156.9C747,123.2,793,92.6,855.6,82l0,0.7 C716.3,106.5,687,221.4,658.9,332.2C640.4,405,622.6,474.4,573.5,509.5z"/>
                  <path d="M595.2,502.3c-11.3,8-24.6,14-40,17.4c-56.8,12.7-112,12.7-160.5,12.9c-60.2,0.1-112,0.2-157,21.1 c-49.5,23-84,69.3-108.5,146l-0.6-0.2c24.3-76.7,58.9-123.1,108.6-146.3c45.1-21.1,97.2-21.1,157.4-21.2 c48.6,0,103.6-0.1,160.5-12.9c81.6-18.3,99-106.7,117.4-200.6c10.7-55,22-112,46.6-158.2C747,108,788.6,77.5,846.5,67.2l0.1,0.8 C718,91.2,695.2,206.9,673.2,318.9C658.3,394.9,643.8,467.8,595.2,502.3z"/>
                  <path d="M615.3,497.4c-13.7,9.7-30.2,16-50.8,18c-44.4,4.6-86.5,5.8-123.6,6.8c-71.2,2-132.8,3.7-182,27.7 C206,575.6,169.8,627,145,711.3l-0.8-0.1c13-44.6,29-79.3,48.6-106.3c18.1-24.9,39.5-43.1,65.6-55.7 c49.5-24.1,110.9-25.8,182.4-27.7c37.1-1,79.3-2.2,123.5-6.7c92.6-9.4,106.2-106.5,120.5-209.2c7.8-55.9,15.9-113.6,37-160 c23.8-52.7,61.6-83.1,115.3-93.4l0.3,0.7c-53.4,10.1-91,40.4-114.6,92.9c-21.1,46.4-29.2,104.1-36.8,159.9 C674.6,386,663.8,463,615.3,497.4z"/>
                  <path d="M634.4,494c-15.5,11-35.2,17.2-60.4,17.3c-12.3,0.1-24.5,0.1-36.1,0.1c-103.7,0-185.5-0.1-246.4,26.4 c-63.5,27.7-103.7,85-130.5,185.5l-0.8-0.1c13.9-52.5,31.3-92.6,53.2-122.9c20.7-28.8,46.2-49.4,77.8-63.2 c61-26.6,142.9-26.4,246.6-26.4c11.7,0.1,23.8,0,36.1-0.1c103.8-0.2,112.9-105.6,122.5-217.2c4.7-56.9,9.9-115.5,27.5-162.4 c20-53.1,54.1-83.7,104.1-93.7l0.1,0.8c-49.5,9.8-83.5,40.3-103.3,93.1c-17.6,46.9-22.7,105.4-27.6,162 C690.1,378.2,682.9,459.6,634.4,494z"/>
                  <path d="M652.7,491.8c-17.9,12.7-40.7,17.7-69.2,15.4C328,486.2,228.3,517.5,177.2,735.2l-0.9-0.3 c25.9-110.7,64-171.6,127-204c66.6-34.2,160.2-34.6,280.3-24.7c32.2,2.6,56.9-4.1,75.4-20.5c42.1-37.4,45.1-118.6,48-204.7 c4-116.5,8.1-236.8,112.1-258.6l0.1,0.8C715.9,44.8,711.8,164.8,707.8,280.9c-3.1,86.3-5.8,167.7-48.3,205.2 C657.3,488.3,655,490.1,652.7,491.8z"/>
                  <path d="M670.6,490.3c-19.3,13.7-44.8,17.9-77.7,12.7c-138.5-21.4-227.1-13-287.3,27 c-55.4,36.8-89.1,101.7-112.4,216.9l-0.9-0.3C215.8,631,249.6,566,305.1,528.9c60.3-40.1,149.1-48.6,288.1-27.3 c35.9,5.5,63,0,82.6-16.9c43.2-37.5,42.2-124.3,40.9-216.1C714.9,151,713,28.8,809.9,7.7l0.1,0.8c-96,21.1-94.3,142.7-92.7,260.6 c1.3,92.1,2.4,179-41.1,216.7C674.3,487.4,672.6,488.9,670.6,490.3z"/>
              </svg>
      </figure>

      <div class="container pt-4 pt-sm-5">
          <div class="row g-xl-5">
              <div class="col-xl-7 mb-5 mb-xl-0">
                  <div class="pe-xxl-4">    
                  <h2 class="mt-3 lh-base text-mute">Hi! , I am  "Soe Moe Thu"
                      <span class="cd-headline clip big-clip is-full-width text-primary mb-0 d-block d-xxl-inline-block">
                          <span class="typed" data-type-text="Senior Web Developer&&Senior Laravel Developer&&Full-Stack Developer&&Web Design&&Web Development&&UI/UX Design"></span>
                      </span>
                  </h2>
                      <p class="mb-0 mt-4 mt-md-5">I am skilled Laravel backend developer with a proven track record building web applications in test-driven environments. Strong problem-solving and execution skills. Highly disciplined, organized, and hardworking, thriving in both independent and collaborative work. Excellent communicator with a team-oriented approach.</p>

                      <!-- Features -->
                      <div class="row mt-5">
                          <div class="col-md-6 mb-3">
                              <div class="d-flex align-items-center">
                                  <a href="https://github.com/thafanseid" target="__blank" class="d-flex">
                                      <figure class="text-primary mb-0">
                                          <svg width="44" height="44" viewBox="0 0 98 96" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M48.854 0C21.839 0 0 22 0 49.217c0 21.756 13.993 40.172 33.405 46.69 2.427.49 3.316-1.059 3.316-2.362 0-1.141-.08-5.052-.08-9.127-13.59 2.934-16.42-5.867-16.42-5.867-2.184-5.704-5.42-7.17-5.42-7.17-4.448-3.015.324-3.015.324-3.015 4.934.326 7.523 5.052 7.523 5.052 4.367 7.496 11.404 5.378 14.235 4.074.404-3.178 1.699-5.378 3.074-6.6-10.839-1.141-22.243-5.378-22.243-24.283 0-5.378 1.94-9.778 5.014-13.2-.485-1.222-2.184-6.275.486-13.038 0 0 4.125-1.304 13.426 5.052a46.97 46.97 0 0 1 12.214-1.63c4.125 0 8.33.571 12.213 1.63 9.302-6.356 13.427-5.052 13.427-5.052 2.67 6.763.97 11.816.485 13.038 3.155 3.422 5.015 7.822 5.015 13.2 0 18.905-11.404 23.06-22.324 24.283 1.78 1.548 3.316 4.481 3.316 9.126 0 6.6-.08 11.897-.08 13.526 0 1.304.89 2.853 3.316 2.364 19.412-6.52 33.405-24.935 33.405-46.691C97.707 22 75.788 0 48.854 0z" fill="#24292f"/></svg>
                                      </figure>
                                      <div class="ms-3 mt-2">
                                          <h6>GitHub</h6>
                                      </div>
                                  </a>
                              </div>
                          </div>
                          <div class="col-md-6 mb-3">
                              <div class="d-flex align-items-center">
                                  <a href="https://www.linkedin.com/in/soe-moe-thu-70bbb1283/" target="__blank" class="d-flex">
                                      <figure class="text-primary mb-0">
                                          <svg width="44" height="44" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 256 256"><g fill="none"><path d="M0 18.338C0 8.216 8.474 0 18.92 0h218.16C247.53 0 256 8.216 256 18.338v219.327C256 247.79 247.53 256 237.08 256H18.92C8.475 256 0 247.791 0 237.668V18.335z" fill="#069"/><path d="M77.796 214.238V98.986H39.488v115.252H77.8zM58.65 83.253c13.356 0 21.671-8.85 21.671-19.91-.25-11.312-8.315-19.915-21.417-19.915-13.111 0-21.674 8.603-21.674 19.914 0 11.06 8.312 19.91 21.169 19.91h.248zM99 214.238h38.305v-64.355c0-3.44.25-6.889 1.262-9.346 2.768-6.885 9.071-14.012 19.656-14.012 13.858 0 19.405 10.568 19.405 26.063v61.65h38.304v-66.082c0-35.399-18.896-51.872-44.099-51.872-20.663 0-29.738 11.549-34.78 19.415h.255V98.99H99.002c.5 10.812-.003 115.252-.003 115.252z" fill="#fff"/></g></svg>
                                      </figure>
                                      <div class="ms-3 mt-2">
                                          <h6>Linkedin</h6>
                                      </div>
                                  </a>
                              </div>
                          </div>
                          <div class="col-md-6 mb-3">
                              <!-- Features item -->
                              <div class="d-flex align-items-center">
                                  <!-- Svg icon -->
                                  <a href="javascript:void(0);" class="d-flex">
                                      <figure class="text-primary mb-0">
                                          <svg xmlns="http://www.w3.org/2000/svg" width="44" height="44" viewBox="0 0 256 256"><path d="M200.533 256H55.467C24.834 256 0 231.166 0 200.533V55.467C0 24.834 24.834 0 55.467 0h145.067C231.166 0 256 24.834 256 55.467v145.067C256 231.166 231.166 256 200.533 256" fill="#00b900"/><path d="M220.792 116.744c0-41.707-41.81-75.64-93.207-75.64-51.4 0-93.205 33.933-93.205 75.64 0 37.39 33.158 68.704 77.95 74.624 3.036.655 7.166 2.003 8.21 4.597.94 2.355.614 6.048.3 8.43l-1.33 7.98c-.407 2.355-1.875 9.216 8.073 5.024s53.68-31.607 73.233-54.116h-.004c13.508-14.812 19.98-29.845 19.98-46.537" fill="#fff"/><g fill="#00b900"><path d="M108.647 96.6h-6.54c-1.003 0-1.815.813-1.815 1.813v40.612c0 .998.813 1.8 1.815 1.8h6.54c1.003 0 1.815-.8 1.815-1.8V98.403c0-1-.813-1.813-1.815-1.813m45 .01H147.1c-1.005 0-1.815.813-1.815 1.813v24.128l-18.613-25.135c-.043-.064-.092-.126-.14-.183l-.01-.013-.143-.143-.098-.08c-.015-.013-.03-.026-.047-.036l-.094-.064c-.017-.013-.036-.02-.055-.032l-.096-.055-.058-.028-.105-.045-.058-.02a.83.83 0 0 0-.11-.036l-.064-.017-.102-.02c-.026-.006-.053-.01-.077-.01-.032-.006-.064-.01-.096-.013l-.094-.006c-.023 0-.043-.002-.064-.002h-6.537c-1.003 0-1.815.813-1.815 1.813v40.612c0 .998.813 1.8 1.815 1.8h6.537c1.005 0 1.818-.8 1.818-1.8v-24.122l18.633 25.167a1.81 1.81 0 0 0 .463.448c.004.004.01.01.017.015l.113.066.05.03a1.1 1.1 0 0 0 .087.041l.087.038.053.02.126.038c.006.002.017.004.026.006a1.75 1.75 0 0 0 .465.06h6.537c1.003 0 1.815-.8 1.815-1.8V98.402c0-1-.813-1.813-1.815-1.813"/><path d="M92.887 130.657H75.122V98.403c0-1.003-.813-1.815-1.813-1.815h-6.54c-1.003 0-1.815.813-1.815 1.815v40.6a1.8 1.8 0 0 0 .508 1.254.09.09 0 0 0 .024.028c.01.008.02.017.028.026a1.81 1.81 0 0 0 1.252.506h26.12c1.003 0 1.813-.815 1.813-1.815v-6.54c0-1.003-.8-1.815-1.813-1.815m96.864-23.897c1.003 0 1.813-.813 1.813-1.815v-6.54c0-1.003-.8-1.815-1.813-1.815h-26.12a1.8 1.8 0 0 0-1.259.512c-.006.006-.015.013-.02.02s-.02.02-.028.032c-.3.324-.503.764-.503 1.25v40.613c0 .486.194.928.508 1.254l.023.026.026.024c.326.314.768.508 1.254.508h26.12c1.003 0 1.813-.813 1.813-1.813v-6.54c0-1.003-.8-1.815-1.813-1.815H172v-6.865h17.762a1.81 1.81 0 0 0 1.813-1.815v-6.537c0-1.003-.8-1.818-1.813-1.818H172v-6.863h17.762z"/></g></svg> 
                                      </figure>
                                      <div class="ms-3 mt-2">
                                          <h6>soemoethudev</h6>
                                      </div>
                                  </a>
                              </div>
                          </div>
                          <div class="col-md-6 mb-3">
                              <!-- Features item -->
                              <div class="d-flex align-items-center">
                                  <!-- Svg icon -->
                                  <a href="https://www.facebook.com/profile.php?id=100025696896117" target="__blank" class="d-flex">
                                      <figure class="text-primary mb-0">
                                          <svg width="44" height="44" viewBox="126.445 2.281 589 589" xmlns="http://www.w3.org/2000/svg"><circle cx="420.945" cy="296.781" fill="#3c5a9a" r="294.5"/><path d="m516.704 92.677h-65.239c-38.715 0-81.777 16.283-81.777 72.402.189 19.554 0 38.281 0 59.357h-44.788v71.271h46.174v205.177h84.847v-206.531h56.002l5.067-70.117h-62.531s.14-31.191 0-40.249c0-22.177 23.076-20.907 24.464-20.907 10.981 0 32.332.032 37.813 0v-70.403z" fill="#fff"/></svg>
                                      </figure>
                                      <div class="ms-3 mt-2">
                                          <h6>Facebook</h6>
                                      </div>
                                  </a>
                              </div>
                          </div>
                      </div> 
                  </div>
              </div>

              <div class="col-md-10 col-xl-5 position-relative mx-auto mt-7 mt-xl-0">
                  <div class="macbook">
                      <div class="inner">
                          <div class="screen">
                          <div class="face-one">
                              <div class="camera"></div>
                              <div class="display">
                              <div class="shade"></div>
                              </div>
                              <span>MacBook Air</span>
                          </div>
                          <img src="http://www.clker.com/cliparts/i/s/H/f/4/T/apple-logo-white.svg" class="logo" />
                          </div>
                          <div class="body">
                          <div class="face-one">
                              <div class="touchpad">
                              </div>
                              <div class="keyboard">
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key space"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              <div class="key f"></div>
                              </div>
                          </div>
                          <div class="pad one"></div>
                          <div class="pad two"></div>
                          <div class="pad three"></div>
                          <div class="pad four"></div>
                          </div>
                      </div>
                      <div class="shadow"></div>
                  </div>
              </div>

          </div>
      </div>
    </section>
    
    <!-- Skills -->
    <section>
      <div class="container">
        <!-- Title -->
        <div class="inner-container-small text-center">
            <h2 class="mb-0 mt-4">Skills</h2>
        </div>
        <div class="row align-items-center mt-3">
          <swiper
          :slides-per-view="5"
    :space-between="50"
    :breakpoints="breakpoints"
    @swiper="onSwiper"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :modules="modules"
    class="swiper"
  >
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/php.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3">PHP</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/laravel.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3 mt-2">Laravel</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/livewire.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3  mt-2">Livewire</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/css.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3  mt-2">HTML/CSS</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/bootstrap.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3 mt-2">Bootstrap</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/api.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3 mt-2">Restful API</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/mysql.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3 mt-2">MySQL</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/firebase.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3 mt-3">Firebase</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
          <div class="d-flex">
              <img src="/images/skills/jquery.svg" class="" width="50" height="50" alt="client-img">
              <h5 class="ms-3 mt-2">jQuery</h5>
          </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-slide">
        <div class="d-flex">
            <img src="/images/skills/vuejs.svg" class="" width="50" height="50" alt="client-img">
            <h5 class="ms-3 mt-2">Vue js</h5>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide></swiper-slide>
    <swiper-slide></swiper-slide>
    <swiper-slide></swiper-slide>
    <swiper-slide></swiper-slide>
    <swiper-slide></swiper-slide>

    
  </swiper>
            <div class="col-md-12">
                <div class="swiper" data-swiper-options='{
                        "slidesPerView": 2, 
                        "spaceBetween": 50,
                        "breakpoints": { 
                            "576": {"slidesPerView": 3}, 
                            "992": {"slidesPerView": 4}, 
                            "1200": {"slidesPerView": 5}
                        }}'>
                    <!-- Slider items -->
                    <div class="swiper-wrapper align-items-center">
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/php.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3">PHP</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/laravel.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2">Laravel</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/livewire.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3  mt-2">Livewire</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/css.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3  mt-2">HTML/CSS</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/bootstrap.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2">Bootstrap</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/api.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2">Restful API</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/mysql.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2">MySQL</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/firebase.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-3">Firebase</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/jquery.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2">jQuery</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/vuejs.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2">Vue js</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/git-icon.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2">Git </h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/digitalocean.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2">Digital Ocean</h5>
                            </div>
                        </div>
                        <div class="swiper-slide">
                            <div class="d-flex">
                                <img src="/images/skills/domain.svg" class="" width="50" height="50" alt="client-img">
                                <h5 class="ms-3 mt-2"> Domain</h5>
                            </div>
                        </div>
                      
                    </div>
                </div>
            </div>
        </div> 
      </div>
    </section>
      <section class="position-relative overflow-hidden" data-bs-theme="">
          <div class="container position-relative">
              <!-- Title -->
              <div class="inner-container-small text-center">
                  <h2 class="mb-0 mt-4">Projects</h2>
              </div>

              <!-- Service list START -->
              <div class="row gy-5 gy-md-7 mt-3">
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-primary text-center mb-4">
                                <img src="/images/projects/LMS_Logo.svg" width="80" height="80" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3">Library Management System</h6>
                              <p class="mb-3">Role - Backend Developer</p>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-center text-primary mb-4">
                                <img class="img-logo" src="/images/projects/ziwathukha.svg" height="80" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3">ZiWa ThuKha Healthcare Services</h6>
                              <p class="mb-3">Role - Backend Developer</p>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-center text-primary mb-4">
                                <img class="img-logo" src="/images/projects/power2d.png" width="80" height="80" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3">Power2d Results System</h6>
                              <p>Role - Frontend Developer </p>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-center text-primary mb-4">
                                <img class="img-logo" src="/images/projects/lotto.png" width="80" height="80" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"> E-Tickets Sale System</h6>
                              <p>Role - Full-Stack Developer </p>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="icon-lg bg-white text-primary rounded-circle mb-4">
                                <img src="/images/projects/LMS_Logo.svg" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"><a href="#">newmm2d_player</a></h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="icon-lg bg-white text-primary rounded-circle mb-4">
                                <img src="/images/projects/LMS_Logo.svg" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"><a href="#">Oli Stock Live Result</a></h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="icon-lg bg-white text-primary rounded-circle mb-4">
                                <img src="/images/projects/LMS_Logo.svg" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"><a href="#">oneoneapps_web</a></h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-center text-primary mb-4">
                                <img src="/images/projects/bandA.svg" width="80" height="80" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"><a href="#">BandA Microfiance System</a></h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-center text-primary mb-4">
                                <img src="/images/projects/mifer.png" width="80" height="80" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3">Ministry of Investment and Foreign Economic Relations</h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="https://mifer.gov.mm/mm" target="__blank">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-center text-primary mb-4">
                                <img src="/images/projects/moswrr.png" width="80" height="80" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"><a href="https://www.moswrr.gov.mm/" target="__blank">Ministry of Social Welfare Relief and Resttlement </a></h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-center text-primary mb-4">
                                <img src="/images/projects/upg.png" width="90" height="120" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"><a href="#">UPG Reward System </a></h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="icon-lg bg-white text-primary rounded-circle mb-4">
                                <img src="/images/projects/LMS_Logo.svg" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"><a href="#">Business Plus </a></h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="#">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
                  <!-- Service item -->
                  <div class="col-md-4">
                      <div class="card bg-light h-100">
                          <div class="card-body pb-0">
                              <!-- Icon -->
                              <div class="text-center text-primary mb-4">
                                <img src="/images/projects/yezin_logo.png" width="80" height="80" alt="">
                              </div>
                              <!-- Content -->
                              <h6 class="mb-3"><a href="#">Library Management System</a></h6>
                              <p>Growing brands online through digital channels.</p>
                          </div>
                          <div class="text-center">Stacks</div>
                          
                          <div class="card-footer bg-light mt-auto pt-2">
                            <span class="badge bg-primary">PHP</span>
                            <span class="badge bg-primary">Laravel</span>
                            <span class="badge bg-primary">MySQL</span>
                            <span class="badge bg-primary">Bootstrap</span>
                            <span class="badge bg-primary">Livewire</span>
                            <span class="badge bg-primary">Apache</span>
                            <span class="badge bg-primary">Reful API</span>
                            <span class="badge bg-primary">JQuery</span>
                            <div class="text-center pt-3">
                                <a class="icon-link icon-link-hover" href="http://opac.yau.edu.mm/" target="__blank">Visit <i class="bi bi-arrow-right"></i> </a>
                            </div>
                          </div>
                      </div>
                  </div>
              </div>
              <!-- Service list END -->
          </div>
      </section>
    </main>
    <!-- Footer START -->
    <footer class="bg-dark position-relative overflow-hidden pb-0 pt-6 pt-lg-8" data-bs-theme="dark">
        <figure class="position-absolute top-0 start-0 mt-n8 ms-n9">
          <svg class="fill-mode" width="775px" height="834px" viewBox="0 0 775 834" style="enable-background:new 0 0 775 834; opacity: 0.05;" xml:space="preserve">
            <path d="M486.1,564.4c-3.6,2.5-7.4,4.8-11.3,6.4c-12,5.5-25.7,7.9-42.2,7.4c-30.6-1.1-65.6-12.5-102.8-24.4 c-50.7-16.2-103.3-33.4-152.5-27c-56.1,7.2-97.9,44.4-128,114l-0.4-0.2c67.5-156.1,181-119.5,281.1-87.1c37,12,72,23.2,102.5,24.3 c34.3,1.2,58.1-10.7,74.9-37.4C530.1,505,547.1,466,565,425.1C619.4,301,675.6,172.7,892.1,141.3l0.1,0.4 c-216.2,31.4-272.5,159.5-326.8,283.5c-18.1,41.1-35,79.7-57.7,115.6C501.6,550.7,494.5,558.5,486.1,564.4z"></path>
            <path d="M500.9,551.4c-43.7,31-103,15.8-165.5-0.2c-49.9-12.7-101.5-25.8-148.7-16.7c-53.3,10.5-93.2,49-121.6,118 l-0.5-0.1c15.3-37.1,33.3-64.7,55.1-84.7c19.5-17.7,41.3-28.6,66.7-33.7c47.4-9.2,99,3.9,148.9,16.6 c70.4,17.9,137.1,34.9,181.3-14.4c35.7-39.9,57.3-91.7,80.2-146.7c23.8-56.7,48.2-115.5,90.2-163.6c22.7-25.9,48.4-46.4,78.4-62.4 c33.9-18.1,72.2-30.3,117.1-37.1l0.1,0.4C695,155.3,645.2,274.5,597.1,389.7c-22.9,55-44.5,106.8-80.4,146.8 C512.3,542.4,506.6,547.3,500.9,551.4z"></path>
            <path d="M521.3,536.4c-21.9,15.5-48.4,23.4-80.8,23.8c-31.2,0.5-65.1-5.8-97.9-11.9c-49.3-9.2-100.2-18.7-145.7-6.5 c-51.1,13.7-88.9,53.7-116,122.6l-0.6-0.2c60.5-154.1,163.3-135,262.6-116.5c68.1,12.7,132.6,24.6,183.6-15.8 c48.1-38.2,71.1-100.6,95.6-166.5c20.3-55,41.4-111.6,78.3-158.1c20-25.1,42.7-44.9,69.2-60.5c30.1-17.5,64.2-29.1,104.3-35.4 l0.2,0.6c-167.2,26.3-210,141.9-251.4,253.5C598.3,431.5,575,493.8,527,532.2C525.1,533.8,523.2,535.1,521.3,536.4z"></path>
            <path d="M548.9,520.3c-4,2.9-8.2,5.6-12.6,8c-56.6,31.5-120.9,23.8-183,16.6c-51.7-6-100.4-11.8-144.6,3.2 c-49.9,16.9-85.5,57.7-111.3,128.2l-0.6-0.2c13.7-37.3,30.1-66,49.9-87.8c17.8-19.4,37.9-32.8,61.8-40.9 c44.3-15,93.1-9.3,144.9-3.2c62.1,7.2,126.3,14.8,182.8-16.6c59.6-33.2,82-104.7,105.9-180.4c17.1-54.3,34.7-110.5,67.2-156.6 c36.7-52,87.8-82.8,155.7-94l0.2,0.6c-151.9,25-187.8,139.3-222.3,250C620.4,417.6,599.4,484.5,548.9,520.3z"></path>
            <path d="M573.5,509.5c-8.2,5.8-17.4,10.7-27.7,14.6c-59.3,22-119.1,18.8-176.8,15.8c-53.2-2.8-103.3-5.3-147.1,12.5 C172.6,572.3,138.1,615.5,113,688l-0.5-0.1c25.1-72.7,59.6-115.9,108.9-136c44-18,94.2-15.3,147.6-12.6 c57.7,3,117.4,6.1,176.6-15.9c70.7-26.2,91.1-106.3,112.8-191.4c13.9-54.5,28.3-111,56.7-156.9C747,123.2,793,92.6,855.6,82l0,0.7 C716.3,106.5,687,221.4,658.9,332.2C640.4,405,622.6,474.4,573.5,509.5z"></path>
            <path d="M595.2,502.3c-11.3,8-24.6,14-40,17.4c-56.8,12.7-112,12.7-160.5,12.9c-60.2,0.1-112,0.2-157,21.1 c-49.5,23-84,69.3-108.5,146l-0.6-0.2c24.3-76.7,58.9-123.1,108.6-146.3c45.1-21.1,97.2-21.1,157.4-21.2 c48.6,0,103.6-0.1,160.5-12.9c81.6-18.3,99-106.7,117.4-200.6c10.7-55,22-112,46.6-158.2C747,108,788.6,77.5,846.5,67.2l0.1,0.8 C718,91.2,695.2,206.9,673.2,318.9C658.3,394.9,643.8,467.8,595.2,502.3z"></path>
            <path d="M615.3,497.4c-13.7,9.7-30.2,16-50.8,18c-44.4,4.6-86.5,5.8-123.6,6.8c-71.2,2-132.8,3.7-182,27.7 C206,575.6,169.8,627,145,711.3l-0.8-0.1c13-44.6,29-79.3,48.6-106.3c18.1-24.9,39.5-43.1,65.6-55.7 c49.5-24.1,110.9-25.8,182.4-27.7c37.1-1,79.3-2.2,123.5-6.7c92.6-9.4,106.2-106.5,120.5-209.2c7.8-55.9,15.9-113.6,37-160 c23.8-52.7,61.6-83.1,115.3-93.4l0.3,0.7c-53.4,10.1-91,40.4-114.6,92.9c-21.1,46.4-29.2,104.1-36.8,159.9 C674.6,386,663.8,463,615.3,497.4z"></path>
            <path d="M634.4,494c-15.5,11-35.2,17.2-60.4,17.3c-12.3,0.1-24.5,0.1-36.1,0.1c-103.7,0-185.5-0.1-246.4,26.4 c-63.5,27.7-103.7,85-130.5,185.5l-0.8-0.1c13.9-52.5,31.3-92.6,53.2-122.9c20.7-28.8,46.2-49.4,77.8-63.2 c61-26.6,142.9-26.4,246.6-26.4c11.7,0.1,23.8,0,36.1-0.1c103.8-0.2,112.9-105.6,122.5-217.2c4.7-56.9,9.9-115.5,27.5-162.4 c20-53.1,54.1-83.7,104.1-93.7l0.1,0.8c-49.5,9.8-83.5,40.3-103.3,93.1c-17.6,46.9-22.7,105.4-27.6,162 C690.1,378.2,682.9,459.6,634.4,494z"></path>
            <path d="M652.7,491.8c-17.9,12.7-40.7,17.7-69.2,15.4C328,486.2,228.3,517.5,177.2,735.2l-0.9-0.3 c25.9-110.7,64-171.6,127-204c66.6-34.2,160.2-34.6,280.3-24.7c32.2,2.6,56.9-4.1,75.4-20.5c42.1-37.4,45.1-118.6,48-204.7 c4-116.5,8.1-236.8,112.1-258.6l0.1,0.8C715.9,44.8,711.8,164.8,707.8,280.9c-3.1,86.3-5.8,167.7-48.3,205.2 C657.3,488.3,655,490.1,652.7,491.8z"></path>
            <path d="M670.6,490.3c-19.3,13.7-44.8,17.9-77.7,12.7c-138.5-21.4-227.1-13-287.3,27 c-55.4,36.8-89.1,101.7-112.4,216.9l-0.9-0.3C215.8,631,249.6,566,305.1,528.9c60.3-40.1,149.1-48.6,288.1-27.3 c35.9,5.5,63,0,82.6-16.9c43.2-37.5,42.2-124.3,40.9-216.1C714.9,151,713,28.8,809.9,7.7l0.1,0.8c-96,21.1-94.3,142.7-92.7,260.6 c1.3,92.1,2.4,179-41.1,216.7C674.3,487.4,672.6,488.9,670.6,490.3z"></path>
          </svg>
        </figure>

      
        <div class="container position-relative">
            <div class="row g-4 justify-content-between">
                <!-- About Us -->
                <div class="col-lg-3">
                    <!-- logo -->
                    <a class="me-0" href="index.html">
                        <img class="light-mode-item h-40px" src="/src/assets/logo.svg" alt="logo">
                        <img class="dark-mode-item h-40px" src="/src/assets/logo.svg" alt="logo">
                    </a>
                    <p class="mt-4 mb-2">A Bootstrap theme that's both stylish and functional, perfect for any type of technology or corporate website.</p>
                </div>

                <div class="col-lg-8 col-xxl-7">
                    <div class="row g-4">
                        <!-- Link block -->
                        <div class="col-6 col-md-4">
                            <h6 class="mb-2 mb-md-4">Quick links</h6>
                            <ul class="nav flex-column">
                                <li class="nav-item"><a class="nav-link pt-0" href="about-v1.html">About us</a></li>
                                <li class="nav-item"><a class="nav-link" href="contact-v1.html">Contact us</a></li>
                            </ul>
                        </div>

                        <!-- Link block -->
                        <div class="col-6 col-md-4">
                            <h6 class="mb-2 mb-md-4">Community</h6>
                            <ul class="nav flex-column">
                                <li class="nav-item"><a class="nav-link pt-0" href="#">StackOverflow</a></li>
                                <li class="nav-item"><a class="nav-link" href="#">Laracast <i class="bi bi-box-arrow-up-right small ms-1"></i></a></li>
                            </ul>
                        </div>

                        <!-- Link block -->
                        <div class="col-md-4">
                            <!-- Social buttons -->
                            <h6 class="mb-2 mb-md-4">Follow on</h6>
                            <ul class="list-inline mb-0 mt-3">
                                <li class="list-inline-item"> <a class="btn btn-xs btn-icon btn-light" href="#"><i class="fab fa-fw fa-facebook-f lh-base"></i></a> </li>
                                <li class="list-inline-item"> <a class="btn btn-xs btn-icon btn-light" href="#"><i class="fab fa-fw fa-instagram lh-base"></i></a> </li>
                                <li class="list-inline-item"> <a class="btn btn-xs btn-icon btn-light" href="#"><i class="fab fa-fw fa-twitter lh-base"></i></a> </li>
                                <li class="list-inline-item"> <a class="btn btn-xs btn-icon btn-light" href="#"><i class="fab fa-fw fa-linkedin-in lh-base"></i></a> </li>
                                <li class="list-inline-item"> <a class="btn btn-xs btn-icon btn-light" href="#"><i class="fab fa-fw fa-youtube lh-base"></i></a> </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <!-- Widget 2 END -->
            </div>

            <!-- Divider -->
            <hr class="mt-4 mb-0">
            <div class="text-lg-start py-4">
              <div class="text-center text-body"> Copyrights ©2024 Soe Moe Thu </div>
            </div>
        </div>
    </footer>
</template>
