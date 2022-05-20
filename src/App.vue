<template>
  <div class="main">
    <div class="banner">

    </div>
    <div class = "mid">
      <header>
        <h1>Ian Duncan McKenzie</h1>
        <h3>Software Developer</h3>
        <div class = "links">
          <a href="https://github.com/Gleep-idm?tab=repositories">GitHub</a>
          ·
          <a href="https://www.linkedin.com/in/ian-mckenzie-05a8a2149">LinkedIn</a>
          ·
          <a href="mailto: ianmckenzie000@gmail.com">Email</a>
        </div>
      </header>

      <div class="row">
        <div class="col">
          <button class="button resume" title="Resume"><img src = "./assets/resume.png"></button>
          <button class="button work" title="Work Experience"><img src = "./assets/work.png"></button>
          <button class="button research" title="Research Interests"><img src = "./assets/research.png"></button>
        </div>
        <div class="col">
          <button class="button projects" title="Personal Projects"><img src = "./assets/projects.png"></button>
          <button class="button school" title="Education"><img src = "./assets/school.png"></button>
          <button class="button hobbies" title="Hobbies"><img src = "./assets/hobbies.png"></button>
        </div>
      </div>
    </div>
    <div class="banner">

    </div>
  </div>
</template>

<script>
export default {
  name: "App"
}
</script>

<style>
@import './assets/base.css';


#app {
  margin: 0 auto;
  height: 100%;
  font-weight: normal;
}

.button[title]:hover::after {
  content: attr(title);
  color: #000000;
  padding-top: 1.5rem;
  font-size: 15px;
}

.main{
  min-height:100%;
  overflow: auto;
}

.main:after {
  display:table;
  content:"";
  clear:both;
}

.row:after {
  display:table;
  content:"";
  clear:both;
}

.mid {
  float: left;
  width: 50%;
  border-width: 12px;
  border-style: solid;
  border-top: 0px;
  border-bottom: 0px;
  height: 100vh;
  border-image:
    linear-gradient(
    to right,
    #000000,
    gray,
    #000000
    )1 100%;
}

.banner{
  background-image: url(./assets/banner.jpg);
  height: 100vh;
  float: left;
  width: 25%;
}

.col {
  display: grid;
  padding: 2rem;
  gap: 40px;
  justify-content: center;
  float: left;
  width: 50%;
}

.button {
  background: linear-gradient(
  45deg,
  #A6A6A6,
  #4C4C4C
  );
  cursor: pointer;
  position: relative;
  z-index: 0;
  border-radius: 100%;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button:before {
  content: "";
  background: linear-gradient(
      45deg,
      #ff0000,
      #ff7300,
      #fffb00,
      #48ff00,
      #00ffd5,
      #002bff,
      #7a00ff,
      #ff00c8,
      #ff0000
  );
  position: absolute;
  top: -2px;
  left: -2px;
  background-size: 400%;
  z-index: -1;
  filter: blur(5px);
  -webkit-filter: blur(5px);
  width: calc(100% + 4px);
  height: calc(100% + 4px);
  animation: glowing-button 20s linear infinite;
  transition: opacity 0.3s ease-in-out;
  border-radius: 100%;
}

@keyframes glowing-button {
  0% {
    background-position: 0 0;
  }
  50% {
    background-position: 400% 0;
  }
  100% {
    background-position: 0 0;
  }
}

.button:after {
  z-index: -1;
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background: linear-gradient(
      45deg,
      #A6A6A6,
      #4C4C4C
  );
  left: 0;
  top: 0;
  border-radius: 100%;
}

button {
  border-radius: 100%;
  width: 10rem;
  height: 10rem;
  padding: 0.6em 2em;
  color: rgb(255, 255, 255);
  background: #111;
}

@keyframes glowing-button-85 {
  0% {
    background-position: 0 0;
  }
  50% {
    background-position: 400% 0;
  }
  100% {
    background-position: 0 0;
  }
}

button:before {
  background: linear-gradient(
      45deg,
      #ff0000,
      #ff7300,
      #fffb00,
      #48ff00,
      #00ffd5,
      #002bff,
      #7a00ff,
      #ff00c8,
      #ff0000
  );
  animation: glowing-button-85 20s linear infinite;
  transition: opacity 0.3s ease-in-out;
}



header {
  text-align: center;
}

header h3 {
  color: var(--color-text-alternate);
  font-size: 2rem;
}

header h1 {
  font-size: 4rem;
  font-family: Georgia, serif;
}
</style>