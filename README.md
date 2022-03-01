/**
  @author denim2x <denim2x@cyberdude.com>
  @license MIT
  
  Pure-CSS Masonry layout, implemented via grid (http://mdn.io/grid);
  all items are being nicely stacked vertically - thanks to 
  `grid-auto-rows` and `grid-row: span ...`.

  SUIT CSS compliant implementation.
 */
@import url('https://fonts.googleapis.com/css?family=Merienda+One');

/* Global variables */
:root {
  --Container-columns: 1;
  --Container-width: 230px;
}

/* The main container */
.Container {
  display: grid;
  grid-auto-rows: 5px;
  
  grid-gap: 10px;
  grid-template-columns: repeat(var(--Container-columns), 1fr);
  
  min-width: 180px;
  max-width: calc(var(--Container-columns) * var(--Container-width));
  
  padding: 0 7px;
  margin: 50px auto 10px;
  
  position: relative;
  box-sizing: border-box;
}

.Container-item {
  --weight: 1;      /* jQuery: $(...).css('--weight', ...); */
  grid-row: span var(--weight);
  
  border-radius: 13px;  
  box-sizing: border-box;
  
  font-size: 1.7em;
  font-weight: 400;
  
  color: hsl(0, 0%, 31%);
  background: hsl(0, 0%, 76%);
}

/* Flexbox layout (http://mdn.io/flexbox) */
.Container-item, .Header {
  display: flex;
  align-items: center;
  justify-content: center;
}

/*  */
.Container-item:nth-child(5n+1) {
  --weight: 16;
}

.Container-item:nth-child(5n+2) {
  --weight: 10;
}

.Container-item:nth-child(5n+3) {
  --weight: 13;
}

.Container-item:nth-child(5n+4) {
  --weight: 11;
}

.Container-item:nth-child(5n) {
  --weight: 13;
}


/* Layout responsiveness (http://mdn.io/@media) */
@media screen and (min-width: 420px) {
  :root {
    --Container-columns: 2;
  }
}

@media screen and (min-width: 600px) {
  :root {
    --Container-columns: 3;
  }
}

@media screen and (min-width: 857px) {
  :root {
    --Container-columns: 4;
  }
}

@media screen and (min-width: 1224px) {
  :root {
    --Container-columns: 5;
  }
}

@media screen and (min-width: 1748px) {
  :root {
    --Container-columns: 6;
  }
}


/* Header styles */
.Header {
  position: fixed;
  z-index: 1;
  
  top: 0;
  left: 0;
  
  width: 100%;
  height: 40px;
  
  padding: 0 5px;
  box-sizing: border-box;
  
  opacity: 0.7;
  background: hsl(0, 0%, 83%);
}

.Header-title {
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
  
  font-size: 1.05em;
  
  color: hsl(0, 0%, 18%);
}


/* Document styles */
body {
  font-family: 'Merienda One', cursive;
  background: hsl(0, 0%, 92%);
}

html, body {
  width: 100%;
  height: 100%;
  
  padding: 0;
  margin: 0;
}

<header class="Header">
  <h1 class="Header-title">CSS-grid Masonry layout</h1>
</header>

<main class="Container">
  <div class="Container-item">1</div>
  <div class="Container-item">2</div>
  <div class="Container-item">3</div>
  <div class="Container-item">4</div>
  <div class="Container-item">5</div>
  <div class="Container-item">6</div>
  <div class="Container-item">7</div>
  <div class="Container-item">8</div>
  <div class="Container-item">9</div>
  <div class="Container-item">10</div>
  <div class="Container-item">11</div>
  <div class="Container-item">12</div>
  <div class="Container-item">13</div>
  <div class="Container-item">14</div>
  <div class="Container-item">15</div>
  <div class="Container-item">16</div>
</main>

<h1 align="center">Hi there, I'm Sorouh Torabi</h1>

<p align="center"> 
 <a href="https://github.com/tspersian" alt="soroush torabi's github stats">
   <img src="https://img.shields.io/badge/-@tspersian-%23181717?style=flat-square&logo=github" />
 </a>
</p>

<p align="center"> 
 <strong>
  Professional skills
  </strong>
</p>

<p align="center">
   <a href="https://dotnet.microsoft.com/">
    <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="php" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
   <a href="https://dotnet.microsoft.com/">
    <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="c#" style="vertical-align:top; margin:4px;width:70px;height:28;">
  </a>
  <a href="https://dotnet.microsoft.com/en-us/apps/xamarin">
    <img src="https://img.shields.io/badge/Xamarin-3498DB?style=for-the-badge&logo=xamarin&logoColor=white" alt="xamarin" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
   <a href="https://dotnet.microsoft.com/">
    <img src="https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white" alt="dotnet" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
  <a href="https://go.dev/">
    <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="golang" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
  <a href="https://www.gnu.org/software/bash/">
    <img src="https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white" alt="shell" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
  <a href="https://vuejs.org/">
    <img src="https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vue.js&logoColor=4FC08D" alt="vuejs" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
  <a href="https://hub.docker.com/">
    <img src="https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" alt="docker" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a> 
 
  <a href="https://kubernetes.io">
    <img src="https://img.shields.io/badge/kubernetes-326ce5.svg?&style=for-the-badge&logo=kubernetes&logoColor=white" alt="kubernetes" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
  <a href="https://www.elastic.co">
    <img src="https://img.shields.io/badge/Elastic_Search-005571?style=for-the-badge&logo=elasticsearch&logoColor=white" alt="elasticsearch" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
  <a href="https://www.rabbitmq.com">
    <img src="https://img.shields.io/badge/rabbitmq-%23FF6600.svg?&style=for-the-badge&logo=rabbitmq&logoColor=white" alt="rabbitmq" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
  <a href="https://microsoft.com">
    <img src="https://img.shields.io/badge/Microsoft_SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white" alt="mssql" style="vertical-align:top; margin:4px;width:70px;height:28px;">
  </a>
  
  <br/>
</p>
<br/>

---

<p align="center">
  <a href="#" alt="soroush torabi's github stats"><img src="https://github-readme-streak-stats.herokuapp.com/?user=tspersian" /></a>
</p>
