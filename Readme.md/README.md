# INDEX.html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Profile</title>
    <link rel="stylesheet" href="./Styles.css">


</head>

<body>
    <nav>
        <section class="nav-links">
            <div class="home">
                
                <a href="index.html"> Home </a>
                <a href="./About-me.html"> About me </a>
            </div>
            <div class="blog-projects">
                <a href="./projects.html"> projects</a>
                <a href="./blog2/blog2.html"> Blog</a>
            </div>
        </section>
        <section class="social-links">
            <a href="https://www.linkedin.com/in/sainath-biradar-7139241a9/">linkedin</a>
            <a href="https://github.com/sainath123-del">Github</a>
        </section>
        <button class="hamburger hamburger--squeezes button-outline" type="button">
            <span class="hamburger-box">
                <span class="hamburger-inner"></span>
            </span>
        </button>
    </nav>
     <ul class="hamburger-links">
        <li><a href="./projects.html">Projects</a></li>
        <li><a href="./">blog</a></li>
        <li><a href="https://www.linkedin.com/in/sainath-biradar-7139241a9/">linkedin</a></li>
        <li><a href="https://github.com/sainath123-del">Github</a></li>
    </ul>
        <main class="main-background">
            <div class="title-container">
                <h1>Ajay Biradar</h1>
                <h2>Software Engineer</h2>
                <!-- <h3>Email-id:Saianthbiradar2@gmail.com</h3> -->
            </div>
        </main>
        <script>
            const hamburger = document.querySelector('.hamburger')
            const links = document.querySelector('.hamburger-links')
            hamburger.addEventListener('click', function () {
                hamburger.classList.toggle('is-active')
                const isActive = hamburger.classList.contains('is-active')
                if (isActive) {
                    links.style.display = 'block'
                } else {
                    links.style.display = 'none'
                }
            })
        </script>
</body>
</htm>




## styles.css
@import "body.css";
@import "nav.css";
@import "main.css";
@import "./hamburger/style.css";
@import "./components/self-me.css";
@import "./hamburger/about-me.css";
@import "./components/globsl.css";
@import "./components/projects.css";
@import "./components/blog.css";

# body.css
body {
    margin: 0px;
    font-family: Arial, Helvetica, sans-serif;
}

# nav.css


nav {
    height: 10vh;
    background: rgb(19, 18, 18);
    display: flex;
    align-items: center;
    justify-content: space-between;

}
nav a {
    color: white;
    text-decoration: none;
    
    font-family: 'Times New Roman', Times, serif;
    margin: 0px, 5px;
}
.nav-links a:hover{
    border-bottom: 1px, solid rgb(153, 73, 73);
}
.nav-links
{
    margin-left: 20px;
    display: flex;
}
.social-links
{
    margin-right: 30px;
}
@media only screen and (max-width: 400px)
{
    .nav a {
        font-size: 10px;
    }
}
.hamburger{
    display: none;
}

@media only screen and (max-width: 500px)
{
    .blog-projects {
        display: none;
    }

    .links {
        display: none;

    }
    .hamburger {
        display: block;
    }
}
.hamburger-links{
    display: none;
}
.hamburger-links {
    display: none;
    background: transparent;
    position: fixed;
    top: 10vh;
    z-index: 2;
    background: white;
    width: 100vw;
    list-style: none;
    margin: 0px;
    padding: 0px;
}
.hamburger-links li {
    text-align: center;
    margin: 10px,0px;

}
.hamburger-links li a{
    text-decoration: none;
    color: black;
}
.hamburger-links li a:hover{
    border-bottom: 1px,solid black;
}

# main.css

# hamburger/style.css

/*!
 * Hamburgers
 * @description Tasty CSS-animated hamburgers
 * @author Jonathan Suh @jonsuh
 * @site https://jonsuh.com/hamburgers
 * @link https://github.com/jonsuh/hamburgers
 */
 .hamburger {
    padding: 15px 15px;
    display: inline-block;
    cursor: pointer;
    transition-property: opacity, filter;
    transition-duration: 0.15s;
    transition-timing-function: linear;
    font: inherit;
    color: inherit;
    text-transform: none;
    background-color: transparent;
    border: 0;
    margin: 0;
    overflow: visible; }
    .hamburger:hover {
      opacity: 0.7; }
    .hamburger.is-active:hover {
      opacity: 0.7; }
    .hamburger.is-active .hamburger-inner,
    .hamburger.is-active .hamburger-inner::before,
    .hamburger.is-active .hamburger-inner::after {
      background-color:whitesmoke; }
  
  .hamburger-box {
    width: 40px;
    height: 24px;
    display: inline-block;
    position: relative; }
  
  .hamburger-inner {
    display: block;
    top: 50%;
    margin-top: -2px; }
    .hamburger-inner, .hamburger-inner::before, .hamburger-inner::after {
      width: 40px;
      height: 4px;
      background-color:whitesmoke;
      border-radius: 4px;
      position: absolute;
      transition-property: transform;
      transition-duration: 0.15s;
      transition-timing-function: ease; }
    .hamburger-inner::before, .hamburger-inner::after {
      content: "";
      display: block; }
    .hamburger-inner::before {
      top: -10px; }
    .hamburger-inner::after {
      bottom: -10px; }
  
  /*
     * 3DX
     */
  .hamburger--3dx .hamburger-box {
    perspective: 80px; }
  
  .hamburger--3dx .hamburger-inner {
    transition: transform 0.15s cubic-bezier(0.645, 0.045, 0.355, 1), background-color 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
    .hamburger--3dx .hamburger-inner::before, .hamburger--3dx .hamburger-inner::after {
      transition: transform 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
  
  .hamburger--3dx.is-active .hamburger-inner {
    background-color: transparent !important;
    transform: rotateY(180deg); }
    .hamburger--3dx.is-active .hamburger-inner::before {
      transform: translate3d(0, 10px, 0) rotate(45deg); }
    .hamburger--3dx.is-active .hamburger-inner::after {
      transform: translate3d(0, -10px, 0) rotate(-45deg); }
  
  /*
     * 3DX Reverse
     */
  .hamburger--3dx-r .hamburger-box {
    perspective: 80px; }
  
  .hamburger--3dx-r .hamburger-inner {
    transition: transform 0.15s cubic-bezier(0.645, 0.045, 0.355, 1), background-color 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
    .hamburger--3dx-r .hamburger-inner::before, .hamburger--3dx-r .hamburger-inner::after {
      transition: transform 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
  
  .hamburger--3dx-r.is-active .hamburger-inner {
    background-color: transparent !important;
    transform: rotateY(-180deg); }
    .hamburger--3dx-r.is-active .hamburger-inner::before {
      transform: translate3d(0, 10px, 0) rotate(45deg); }
    .hamburger--3dx-r.is-active .hamburger-inner::after {
      transform: translate3d(0, -10px, 0) rotate(-45deg); }
  
  /*
     * 3DY
     */
  .hamburger--3dy .hamburger-box {
    perspective: 80px; }
  
  .hamburger--3dy .hamburger-inner {
    transition: transform 0.15s cubic-bezier(0.645, 0.045, 0.355, 1), background-color 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
    .hamburger--3dy .hamburger-inner::before, .hamburger--3dy .hamburger-inner::after {
      transition: transform 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
  
  .hamburger--3dy.is-active .hamburger-inner {
    background-color: transparent !important;
    transform: rotateX(-180deg); }
    .hamburger--3dy.is-active .hamburger-inner::before {
      transform: translate3d(0, 10px, 0) rotate(45deg); }
    .hamburger--3dy.is-active .hamburger-inner::after {
      transform: translate3d(0, -10px, 0) rotate(-45deg); }
  
  /*
     * 3DY Reverse
     */
  .hamburger--3dy-r .hamburger-box {
    perspective: 80px; }
  
  .hamburger--3dy-r .hamburger-inner {
    transition: transform 0.15s cubic-bezier(0.645, 0.045, 0.355, 1), background-color 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
    .hamburger--3dy-r .hamburger-inner::before, .hamburger--3dy-r .hamburger-inner::after {
      transition: transform 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
  
  .hamburger--3dy-r.is-active .hamburger-inner {
    background-color: transparent !important;
    transform: rotateX(180deg); }
    .hamburger--3dy-r.is-active .hamburger-inner::before {
      transform: translate3d(0, 10px, 0) rotate(45deg); }
    .hamburger--3dy-r.is-active .hamburger-inner::after {
      transform: translate3d(0, -10px, 0) rotate(-45deg); }
  
  /*
     * 3DXY
     */
  .hamburger--3dxy .hamburger-box {
    perspective: 80px; }
  
  .hamburger--3dxy .hamburger-inner {
    transition: transform 0.15s cubic-bezier(0.645, 0.045, 0.355, 1), background-color 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
    .hamburger--3dxy .hamburger-inner::before, .hamburger--3dxy .hamburger-inner::after {
      transition: transform 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
  
  .hamburger--3dxy.is-active .hamburger-inner {
    background-color: transparent !important;
    transform: rotateX(180deg) rotateY(180deg); }
    .hamburger--3dxy.is-active .hamburger-inner::before {
      transform: translate3d(0, 10px, 0) rotate(45deg); }
    .hamburger--3dxy.is-active .hamburger-inner::after {
      transform: translate3d(0, -10px, 0) rotate(-45deg); }
  
  /*
     * 3DXY Reverse
     */
  .hamburger--3dxy-r .hamburger-box {
    perspective: 80px; }
  
  .hamburger--3dxy-r .hamburger-inner {
    transition: transform 0.15s cubic-bezier(0.645, 0.045, 0.355, 1), background-color 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
    .hamburger--3dxy-r .hamburger-inner::before, .hamburger--3dxy-r .hamburger-inner::after {
      transition: transform 0s 0.1s cubic-bezier(0.645, 0.045, 0.355, 1); }
  
  .hamburger--3dxy-r.is-active .hamburger-inner {
    background-color: transparent !important;
    transform: rotateX(180deg) rotateY(180deg) rotateZ(-180deg); }
    .hamburger--3dxy-r.is-active .hamburger-inner::before {
      transform: translate3d(0, 10px, 0) rotate(45deg); }
    .hamburger--3dxy-r.is-active .hamburger-inner::after {
      transform: translate3d(0, -10px, 0) rotate(-45deg); }
  
  /*
     * Arrow
     */
  .hamburger--arrow.is-active .hamburger-inner::before {
    transform: translate3d(-8px, 0, 0) rotate(-45deg) scale(0.7, 1); }
  
  .hamburger--arrow.is-active .hamburger-inner::after {
    transform: translate3d(-8px, 0, 0) rotate(45deg) scale(0.7, 1); }
  
  /*
     * Arrow Right
     */
  .hamburger--arrow-r.is-active .hamburger-inner::before {
    transform: translate3d(8px, 0, 0) rotate(45deg) scale(0.7, 1); }
  
  .hamburger--arrow-r.is-active .hamburger-inner::after {
    transform: translate3d(8px, 0, 0) rotate(-45deg) scale(0.7, 1); }
  
  /*
     * Arrow Alt
     */
  .hamburger--arrowalt .hamburger-inner::before {
    transition: top 0.1s 0.1s ease, transform 0.1s cubic-bezier(0.165, 0.84, 0.44, 1); }
  
  .hamburger--arrowalt .hamburger-inner::after {
    transition: bottom 0.1s 0.1s ease, transform 0.1s cubic-bezier(0.165, 0.84, 0.44, 1); }
  
  .hamburger--arrowalt.is-active .hamburger-inner::before {
    top: 0;
    transform: translate3d(-8px, -10px, 0) rotate(-45deg) scale(0.7, 1);
    transition: top 0.1s ease, transform 0.1s 0.1s cubic-bezier(0.895, 0.03, 0.685, 0.22); }
  
  .hamburger--arrowalt.is-active .hamburger-inner::after {
    bottom: 0;
    transform: translate3d(-8px, 10px, 0) rotate(45deg) scale(0.7, 1);
    transition: bottom 0.1s ease, transform 0.1s 0.1s cubic-bezier(0.895, 0.03, 0.685, 0.22); }
  
  /*
     * Arrow Alt Right
     */
  .hamburger--arrowalt-r .hamburger-inner::before {
    transition: top 0.1s 0.1s ease, transform 0.1s cubic-bezier(0.165, 0.84, 0.44, 1); }
  
  .hamburger--arrowalt-r .hamburger-inner::after {
    transition: bottom 0.1s 0.1s ease, transform 0.1s cubic-bezier(0.165, 0.84, 0.44, 1); }
  
  .hamburger--arrowalt-r.is-active .hamburger-inner::before {
    top: 0;
    transform: translate3d(8px, -10px, 0) rotate(45deg) scale(0.7, 1);
    transition: top 0.1s ease, transform 0.1s 0.1s cubic-bezier(0.895, 0.03, 0.685, 0.22); }
  
  .hamburger--arrowalt-r.is-active .hamburger-inner::after {
    bottom: 0;
    transform: translate3d(8px, 10px, 0) rotate(-45deg) scale(0.7, 1);
    transition: bottom 0.1s ease, transform 0.1s 0.1s cubic-bezier(0.895, 0.03, 0.685, 0.22); }
  
  /*
     * Arrow Turn
     */
  .hamburger--arrowturn.is-active .hamburger-inner {
    transform: rotate(-180deg); }
    .hamburger--arrowturn.is-active .hamburger-inner::before {
      transform: translate3d(8px, 0, 0) rotate(45deg) scale(0.7, 1); }
    .hamburger--arrowturn.is-active .hamburger-inner::after {
      transform: translate3d(8px, 0, 0) rotate(-45deg) scale(0.7, 1); }
  
  /*
     * Arrow Turn Right
     */
  .hamburger--arrowturn-r.is-active .hamburger-inner {
    transform: rotate(-180deg); }
    .hamburger--arrowturn-r.is-active .hamburger-inner::before {
      transform: translate3d(-8px, 0, 0) rotate(-45deg) scale(0.7, 1); }
    .hamburger--arrowturn-r.is-active .hamburger-inner::after {
      transform: translate3d(-8px, 0, 0) rotate(45deg) scale(0.7, 1); }
  
  /*
     * Boring
     */
  .hamburger--boring .hamburger-inner, .hamburger--boring .hamburger-inner::before, .hamburger--boring .hamburger-inner::after {
    transition-property: none; }
  
  .hamburger--boring.is-active .hamburger-inner {
    transform: rotate(45deg); }
    .hamburger--boring.is-active .hamburger-inner::before {
      top: 0;
      opacity: 0; }
    .hamburger--boring.is-active .hamburger-inner::after {
      bottom: 0;
      transform: rotate(-90deg); }
  
  /*
     * Collapse
     */
  .hamburger--collapse .hamburger-inner {
    top: auto;
    bottom: 0;
    transition-duration: 0.13s;
    transition-delay: 0.13s;
    transition-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--collapse .hamburger-inner::after {
      top: -20px;
      transition: top 0.2s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1), opacity 0.1s linear; }
    .hamburger--collapse .hamburger-inner::before {
      transition: top 0.12s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1), transform 0.13s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--collapse.is-active .hamburger-inner {
    transform: translate3d(0, -10px, 0) rotate(-45deg);
    transition-delay: 0.22s;
    transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1); }
    .hamburger--collapse.is-active .hamburger-inner::after {
      top: 0;
      opacity: 0;
      transition: top 0.2s cubic-bezier(0.33333, 0, 0.66667, 0.33333), opacity 0.1s 0.22s linear; }
    .hamburger--collapse.is-active .hamburger-inner::before {
      top: 0;
      transform: rotate(-90deg);
      transition: top 0.1s 0.16s cubic-bezier(0.33333, 0, 0.66667, 0.33333), transform 0.13s 0.25s cubic-bezier(0.215, 0.61, 0.355, 1); }
  
  /*
     * Collapse Reverse
     */
  .hamburger--collapse-r .hamburger-inner {
    top: auto;
    bottom: 0;
    transition-duration: 0.13s;
    transition-delay: 0.13s;
    transition-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--collapse-r .hamburger-inner::after {
      top: -20px;
      transition: top 0.2s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1), opacity 0.1s linear; }
    .hamburger--collapse-r .hamburger-inner::before {
      transition: top 0.12s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1), transform 0.13s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--collapse-r.is-active .hamburger-inner {
    transform: translate3d(0, -10px, 0) rotate(45deg);
    transition-delay: 0.22s;
    transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1); }
    .hamburger--collapse-r.is-active .hamburger-inner::after {
      top: 0;
      opacity: 0;
      transition: top 0.2s cubic-bezier(0.33333, 0, 0.66667, 0.33333), opacity 0.1s 0.22s linear; }
    .hamburger--collapse-r.is-active .hamburger-inner::before {
      top: 0;
      transform: rotate(90deg);
      transition: top 0.1s 0.16s cubic-bezier(0.33333, 0, 0.66667, 0.33333), transform 0.13s 0.25s cubic-bezier(0.215, 0.61, 0.355, 1); }
  
  /*
     * Elastic
     */
  .hamburger--elastic .hamburger-inner {
    top: 2px;
    transition-duration: 0.275s;
    transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55); }
    .hamburger--elastic .hamburger-inner::before {
      top: 10px;
      transition: opacity 0.125s 0.275s ease; }
    .hamburger--elastic .hamburger-inner::after {
      top: 20px;
      transition: transform 0.275s cubic-bezier(0.68, -0.55, 0.265, 1.55); }
  
  .hamburger--elastic.is-active .hamburger-inner {
    transform: translate3d(0, 10px, 0) rotate(135deg);
    transition-delay: 0.075s; }
    .hamburger--elastic.is-active .hamburger-inner::before {
      transition-delay: 0s;
      opacity: 0; }
    .hamburger--elastic.is-active .hamburger-inner::after {
      transform: translate3d(0, -20px, 0) rotate(-270deg);
      transition-delay: 0.075s; }
  
  /*
     * Elastic Reverse
     */
  .hamburger--elastic-r .hamburger-inner {
    top: 2px;
    transition-duration: 0.275s;
    transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55); }
    .hamburger--elastic-r .hamburger-inner::before {
      top: 10px;
      transition: opacity 0.125s 0.275s ease; }
    .hamburger--elastic-r .hamburger-inner::after {
      top: 20px;
      transition: transform 0.275s cubic-bezier(0.68, -0.55, 0.265, 1.55); }
  
  .hamburger--elastic-r.is-active .hamburger-inner {
    transform: translate3d(0, 10px, 0) rotate(-135deg);
    transition-delay: 0.075s; }
    .hamburger--elastic-r.is-active .hamburger-inner::before {
      transition-delay: 0s;
      opacity: 0; }
    .hamburger--elastic-r.is-active .hamburger-inner::after {
      transform: translate3d(0, -20px, 0) rotate(270deg);
      transition-delay: 0.075s; }
  
  /*
     * Emphatic
     */
  .hamburger--emphatic {
    overflow: hidden; }
    .hamburger--emphatic .hamburger-inner {
      transition: background-color 0.125s 0.175s ease-in; }
      .hamburger--emphatic .hamburger-inner::before {
        left: 0;
        transition: transform 0.125s cubic-bezier(0.6, 0.04, 0.98, 0.335), top 0.05s 0.125s linear, left 0.125s 0.175s ease-in; }
      .hamburger--emphatic .hamburger-inner::after {
        top: 10px;
        right: 0;
        transition: transform 0.125s cubic-bezier(0.6, 0.04, 0.98, 0.335), top 0.05s 0.125s linear, right 0.125s 0.175s ease-in; }
    .hamburger--emphatic.is-active .hamburger-inner {
      transition-delay: 0s;
      transition-timing-function: ease-out;
      background-color: transparent !important; }
      .hamburger--emphatic.is-active .hamburger-inner::before {
        left: -80px;
        top: -80px;
        transform: translate3d(80px, 80px, 0) rotate(45deg);
        transition: left 0.125s ease-out, top 0.05s 0.125s linear, transform 0.125s 0.175s cubic-bezier(0.075, 0.82, 0.165, 1); }
      .hamburger--emphatic.is-active .hamburger-inner::after {
        right: -80px;
        top: -80px;
        transform: translate3d(-80px, 80px, 0) rotate(-45deg);
        transition: right 0.125s ease-out, top 0.05s 0.125s linear, transform 0.125s 0.175s cubic-bezier(0.075, 0.82, 0.165, 1); }
  
  /*
     * Emphatic Reverse
     */
  .hamburger--emphatic-r {
    overflow: hidden; }
    .hamburger--emphatic-r .hamburger-inner {
      transition: background-color 0.125s 0.175s ease-in; }
      .hamburger--emphatic-r .hamburger-inner::before {
        left: 0;
        transition: transform 0.125s cubic-bezier(0.6, 0.04, 0.98, 0.335), top 0.05s 0.125s linear, left 0.125s 0.175s ease-in; }
      .hamburger--emphatic-r .hamburger-inner::after {
        top: 10px;
        right: 0;
        transition: transform 0.125s cubic-bezier(0.6, 0.04, 0.98, 0.335), top 0.05s 0.125s linear, right 0.125s 0.175s ease-in; }
    .hamburger--emphatic-r.is-active .hamburger-inner {
      transition-delay: 0s;
      transition-timing-function: ease-out;
      background-color: transparent !important; }
      .hamburger--emphatic-r.is-active .hamburger-inner::before {
        left: -80px;
        top: 80px;
        transform: translate3d(80px, -80px, 0) rotate(-45deg);
        transition: left 0.125s ease-out, top 0.05s 0.125s linear, transform 0.125s 0.175s cubic-bezier(0.075, 0.82, 0.165, 1); }
      .hamburger--emphatic-r.is-active .hamburger-inner::after {
        right: -80px;
        top: 80px;
        transform: translate3d(-80px, -80px, 0) rotate(45deg);
        transition: right 0.125s ease-out, top 0.05s 0.125s linear, transform 0.125s 0.175s cubic-bezier(0.075, 0.82, 0.165, 1); }
  
  /*
     * Minus
     */
  .hamburger--minus .hamburger-inner::before, .hamburger--minus .hamburger-inner::after {
    transition: bottom 0.08s 0s ease-out, top 0.08s 0s ease-out, opacity 0s linear; }
  
  .hamburger--minus.is-active .hamburger-inner::before, .hamburger--minus.is-active .hamburger-inner::after {
    opacity: 0;
    transition: bottom 0.08s ease-out, top 0.08s ease-out, opacity 0s 0.08s linear; }
  
  .hamburger--minus.is-active .hamburger-inner::before {
    top: 0; }
  
  .hamburger--minus.is-active .hamburger-inner::after {
    bottom: 0; }
  
  /*
     * Slider
     */
  .hamburger--slider .hamburger-inner {
    top: 2px; }
    .hamburger--slider .hamburger-inner::before {
      top: 10px;
      transition-property: transform, opacity;
      transition-timing-function: ease;
      transition-duration: 0.15s; }
    .hamburger--slider .hamburger-inner::after {
      top: 20px; }
  
  .hamburger--slider.is-active .hamburger-inner {
    transform: translate3d(0, 10px, 0) rotate(45deg); }
    .hamburger--slider.is-active .hamburger-inner::before {
      transform: rotate(-45deg) translate3d(-5.71429px, -6px, 0);
      opacity: 0; }
    .hamburger--slider.is-active .hamburger-inner::after {
      transform: translate3d(0, -20px, 0) rotate(-90deg); }
  
  /*
     * Slider Reverse
     */
  .hamburger--slider-r .hamburger-inner {
    top: 2px; }
    .hamburger--slider-r .hamburger-inner::before {
      top: 10px;
      transition-property: transform, opacity;
      transition-timing-function: ease;
      transition-duration: 0.15s; }
    .hamburger--slider-r .hamburger-inner::after {
      top: 20px; }
  
  .hamburger--slider-r.is-active .hamburger-inner {
    transform: translate3d(0, 10px, 0) rotate(-45deg); }
    .hamburger--slider-r.is-active .hamburger-inner::before {
      transform: rotate(45deg) translate3d(5.71429px, -6px, 0);
      opacity: 0; }
    .hamburger--slider-r.is-active .hamburger-inner::after {
      transform: translate3d(0, -20px, 0) rotate(90deg); }
  
  /*
     * Spin
     */
  .hamburger--spin .hamburger-inner {
    transition-duration: 0.22s;
    transition-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--spin .hamburger-inner::before {
      transition: top 0.1s 0.25s ease-in, opacity 0.1s ease-in; }
    .hamburger--spin .hamburger-inner::after {
      transition: bottom 0.1s 0.25s ease-in, transform 0.22s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--spin.is-active .hamburger-inner {
    transform: rotate(225deg);
    transition-delay: 0.12s;
    transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1); }
    .hamburger--spin.is-active .hamburger-inner::before {
      top: 0;
      opacity: 0;
      transition: top 0.1s ease-out, opacity 0.1s 0.12s ease-out; }
    .hamburger--spin.is-active .hamburger-inner::after {
      bottom: 0;
      transform: rotate(-90deg);
      transition: bottom 0.1s ease-out, transform 0.22s 0.12s cubic-bezier(0.215, 0.61, 0.355, 1); }
  
  /*
     * Spin Reverse
     */
  .hamburger--spin-r .hamburger-inner {
    transition-duration: 0.22s;
    transition-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--spin-r .hamburger-inner::before {
      transition: top 0.1s 0.25s ease-in, opacity 0.1s ease-in; }
    .hamburger--spin-r .hamburger-inner::after {
      transition: bottom 0.1s 0.25s ease-in, transform 0.22s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--spin-r.is-active .hamburger-inner {
    transform: rotate(-225deg);
    transition-delay: 0.12s;
    transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1); }
    .hamburger--spin-r.is-active .hamburger-inner::before {
      top: 0;
      opacity: 0;
      transition: top 0.1s ease-out, opacity 0.1s 0.12s ease-out; }
    .hamburger--spin-r.is-active .hamburger-inner::after {
      bottom: 0;
      transform: rotate(90deg);
      transition: bottom 0.1s ease-out, transform 0.22s 0.12s cubic-bezier(0.215, 0.61, 0.355, 1); }
  
  /*
     * Spring
     */
  .hamburger--spring .hamburger-inner {
    top: 2px;
    transition: background-color 0s 0.13s linear; }
    .hamburger--spring .hamburger-inner::before {
      top: 10px;
      transition: top 0.1s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1), transform 0.13s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--spring .hamburger-inner::after {
      top: 20px;
      transition: top 0.2s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1), transform 0.13s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--spring.is-active .hamburger-inner {
    transition-delay: 0.22s;
    background-color: transparent !important; }
    .hamburger--spring.is-active .hamburger-inner::before {
      top: 0;
      transition: top 0.1s 0.15s cubic-bezier(0.33333, 0, 0.66667, 0.33333), transform 0.13s 0.22s cubic-bezier(0.215, 0.61, 0.355, 1);
      transform: translate3d(0, 10px, 0) rotate(45deg); }
    .hamburger--spring.is-active .hamburger-inner::after {
      top: 0;
      transition: top 0.2s cubic-bezier(0.33333, 0, 0.66667, 0.33333), transform 0.13s 0.22s cubic-bezier(0.215, 0.61, 0.355, 1);
      transform: translate3d(0, 10px, 0) rotate(-45deg); }
  
  /*
     * Spring Reverse
     */
  .hamburger--spring-r .hamburger-inner {
    top: auto;
    bottom: 0;
    transition-duration: 0.13s;
    transition-delay: 0s;
    transition-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--spring-r .hamburger-inner::after {
      top: -20px;
      transition: top 0.2s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1), opacity 0s linear; }
    .hamburger--spring-r .hamburger-inner::before {
      transition: top 0.1s 0.2s cubic-bezier(0.33333, 0.66667, 0.66667, 1), transform 0.13s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--spring-r.is-active .hamburger-inner {
    transform: translate3d(0, -10px, 0) rotate(-45deg);
    transition-delay: 0.22s;
    transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1); }
    .hamburger--spring-r.is-active .hamburger-inner::after {
      top: 0;
      opacity: 0;
      transition: top 0.2s cubic-bezier(0.33333, 0, 0.66667, 0.33333), opacity 0s 0.22s linear; }
    .hamburger--spring-r.is-active .hamburger-inner::before {
      top: 0;
      transform: rotate(90deg);
      transition: top 0.1s 0.15s cubic-bezier(0.33333, 0, 0.66667, 0.33333), transform 0.13s 0.22s cubic-bezier(0.215, 0.61, 0.355, 1); }
  
  /*
     * Stand
     */
  .hamburger--stand .hamburger-inner {
    transition: transform 0.075s 0.15s cubic-bezier(0.55, 0.055, 0.675, 0.19), background-color 0s 0.075s linear; }
    .hamburger--stand .hamburger-inner::before {
      transition: top 0.075s 0.075s ease-in, transform 0.075s 0s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--stand .hamburger-inner::after {
      transition: bottom 0.075s 0.075s ease-in, transform 0.075s 0s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--stand.is-active .hamburger-inner {
    transform: rotate(90deg);
    background-color: transparent !important;
    transition: transform 0.075s 0s cubic-bezier(0.215, 0.61, 0.355, 1), background-color 0s 0.15s linear; }
    .hamburger--stand.is-active .hamburger-inner::before {
      top: 0;
      transform: rotate(-45deg);
      transition: top 0.075s 0.1s ease-out, transform 0.075s 0.15s cubic-bezier(0.215, 0.61, 0.355, 1); }
    .hamburger--stand.is-active .hamburger-inner::after {
      bottom: 0;
      transform: rotate(45deg);
      transition: bottom 0.075s 0.1s ease-out, transform 0.075s 0.15s cubic-bezier(0.215, 0.61, 0.355, 1); }
  
  /*
     * Stand Reverse
     */
  .hamburger--stand-r .hamburger-inner {
    transition: transform 0.075s 0.15s cubic-bezier(0.55, 0.055, 0.675, 0.19), background-color 0s 0.075s linear; }
    .hamburger--stand-r .hamburger-inner::before {
      transition: top 0.075s 0.075s ease-in, transform 0.075s 0s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--stand-r .hamburger-inner::after {
      transition: bottom 0.075s 0.075s ease-in, transform 0.075s 0s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--stand-r.is-active .hamburger-inner {
    transform: rotate(-90deg);
    background-color: transparent !important;
    transition: transform 0.075s 0s cubic-bezier(0.215, 0.61, 0.355, 1), background-color 0s 0.15s linear; }
    .hamburger--stand-r.is-active .hamburger-inner::before {
      top: 0;
      transform: rotate(-45deg);
      transition: top 0.075s 0.1s ease-out, transform 0.075s 0.15s cubic-bezier(0.215, 0.61, 0.355, 1); }
    .hamburger--stand-r.is-active .hamburger-inner::after {
      bottom: 0;
      transform: rotate(45deg);
      transition: bottom 0.075s 0.1s ease-out, transform 0.075s 0.15s cubic-bezier(0.215, 0.61, 0.355, 1); }
  
  /*
     * Squeeze
     */
  .hamburger--squeeze .hamburger-inner {
    transition-duration: 0.075s;
    transition-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19); }
    .hamburger--squeeze .hamburger-inner::before {
      transition: top 0.075s 0.12s ease, opacity 0.075s ease; }
    .hamburger--squeeze .hamburger-inner::after {
      transition: bottom 0.075s 0.12s ease, transform 0.075s cubic-bezier(0.55, 0.055, 0.675, 0.19); }
  
  .hamburger--squeeze.is-active .hamburger-inner {
    transform: rotate(45deg);
    transition-delay: 0.12s;
    transition-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1); }
    .hamburger--squeeze.is-active .hamburger-inner::before {
      top: 0;
      opacity: 0;
      transition: top 0.075s ease, opacity 0.075s 0.12s ease; }
    .hamburger--squeeze.is-active .hamburger-inner::after {
      bottom: 0;
      transform: rotate(-90deg);
      transition: bottom 0.075s ease, transform 0.075s 0.12s cubic-bezier(0.215, 0.61, 0.355, 1); }
  
  /*
     * Vortex
     */
  .hamburger--vortex .hamburger-inner {
    transition-duration: 0.2s;
    transition-timing-function: cubic-bezier(0.19, 1, 0.22, 1); }
    .hamburger--vortex .hamburger-inner::before, .hamburger--vortex .hamburger-inner::after {
      transition-duration: 0s;
      transition-delay: 0.1s;
      transition-timing-function: linear; }
    .hamburger--vortex .hamburger-inner::before {
      transition-property: top, opacity; }
    .hamburger--vortex .hamburger-inner::after {
      transition-property: bottom, transform; }
  
  .hamburger--vortex.is-active .hamburger-inner {
    transform: rotate(765deg);
    transition-timing-function: cubic-bezier(0.19, 1, 0.22, 1); }
    .hamburger--vortex.is-active .hamburger-inner::before, .hamburger--vortex.is-active .hamburger-inner::after {
      transition-delay: 0s; }
    .hamburger--vortex.is-active .hamburger-inner::before {
      top: 0;
      opacity: 0; }
    .hamburger--vortex.is-active .hamburger-inner::after {
      bottom: 0;
      transform: rotate(90deg); }
  
  /*
     * Vortex Reverse
     */
  .hamburger--vortex-r .hamburger-inner {
    transition-duration: 0.2s;
    transition-timing-function: cubic-bezier(0.19, 1, 0.22, 1); }
    .hamburger--vortex-r .hamburger-inner::before, .hamburger--vortex-r .hamburger-inner::after {
      transition-duration: 0s;
      transition-delay: 0.1s;
      transition-timing-function: linear; }
    .hamburger--vortex-r .hamburger-inner::before {
      transition-property: top, opacity; }
    .hamburger--vortex-r .hamburger-inner::after {
      transition-property: bottom, transform; }
  
  .hamburger--vortex-r.is-active .hamburger-inner {
    transform: rotate(-765deg);
    transition-timing-function: cubic-bezier(0.19, 1, 0.22, 1); }
    .hamburger--vortex-r.is-active .hamburger-inner::before, .hamburger--vortex-r.is-active .hamburger-inner::after {
      transition-delay: 0s; }
    .hamburger--vortex-r.is-active .hamburger-inner::before {
      top: 0;
      opacity: 0; }
    .hamburger--vortex-r.is-active .hamburger-inner::after {
      bottom: 0;
      transform: rotate(-90deg); }

    











    