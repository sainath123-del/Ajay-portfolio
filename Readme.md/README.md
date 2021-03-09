<!-- <!-- # INDEX.html
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

## nav.css


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

## main.css 
 .main-background {
    background-image: url("./kristopher-roller-zepnJQycr4U-unsplash.jpg"), linear-gradient(to bottom, black, black); 
    height: 90vh;
    background-position:center;
    background-size: cover;
    display: flex;
    justify-content: center;
    filter: rgb(194, 152, 73);
    
    
}
@media only screen and (max-width:700px)
{
main
{
 background-position: left;
}
}
main h1{
    margin: 0px;
    color: rgb(160, 86, 86);
    font-size: 70px;
    color: black;
    text-align: center;
}
main .title-container {
    height: 50%;

    display: flex;
    flex-direction: column;

    justify-content: flex-end;
    align-items: center;

}
@media only screen and (max-width: 750px)
{
    main h1{
        font-size: 40px;
    }
}

## hamburger/style.css
 
