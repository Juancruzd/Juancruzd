<style>
 html {
    height: 100%;
}
body {
	background: #bcdee7 url("http://victory-design.ru/sandbox/codepen/profile_card/bg.png") no-repeat center center fixed;
    background-size: 120% auto;
    position: fixed;
	padding: 0px;
	margin: 0px;
	width: 100%;
	height: 100%;
	font: normal 14px/1.618em "Hind", sans-serif;
	-webkit-font-smoothing: antialiased;
}
body:before {
    content: "";
    height: 0px;
    padding: 0px;
    border: 110em solid #313440;
	position: absolute;
	left: 50%;
	top: 100%;
    z-index: 2;
    display: block;
    -webkit-border-radius: 50%;
    border-radius: 50%;
	-webkit-transform: translate(-50%, -50%);
	transform: translate(-50%, -50%);
    -webkit-animation: puff_portrait 0.5s 1.8s cubic-bezier(0.55, 0.055, 0.675, 0.19) forwards, borderRadius 0.2s 2.3s linear forwards;
    animation: puff_portrait 0.5s 1.8s cubic-bezier(0.55, 0.055, 0.675, 0.19) forwards, borderRadius 0.2s 2.3s linear forwards;
}
h1, h2 {
    font-weight: 400;
    margin: 0px 0px 5px 0px;
}
h1 {
    font-size: 24px;
}
h2 {
    font-size: 16px;
}
p {
    margin: 0px;
}
.profile-card {
	background: #FFB300;
	width: 56px;
	height: 56px;
	position: absolute;
	left: 50%;
	top: 50%;
    z-index: 2;
	overflow: hidden;
    opacity: 0;
    margin-top: 70px;
	-webkit-transform: translate(-50%, -50%);
	transform: translate(-50%, -50%);
	-webkit-border-radius: 50%;
	border-radius: 50%;
	-webkit-box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.16), 0px 3px 6px rgba(0, 0, 0, 0.23);
	box-shadow: 0px 3px 6px rgba(0 ,0, 0, 0.16), 0px 3px 6px rgba(0, 0, 0, 0.23);
    -webkit-animation: init 0.5s 0.2s cubic-bezier(0.55, 0.055, 0.675, 0.19) forwards, moveDown 1s 0.8s cubic-bezier(0.6, -0.28, 0.735, 0.045) forwards, moveUp 1s 1.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards, materia_landscape 0.5s 2.7s cubic-bezier(0.86, 0, 0.07, 1) forwards;
    animation: init 0.5s 0.2s cubic-bezier(0.55, 0.055, 0.675, 0.19) forwards, moveDown 1s 0.8s cubic-bezier(0.6, -0.28, 0.735, 0.045) forwards, moveUp 1s 1.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards, materia_landscape 0.5s 2.7s cubic-bezier(0.86, 0, 0.07, 1) forwards;
}
.profile-card header {
    width: 179px;
    height: 280px;
    padding: 40px 20px 30px 20px;
    display: inline-block;
    float: left;
    border-right: 2px dashed #EEEEEE;
	background: #FFFFFF;
    color: #000000;
    margin-top: 50px;
    opacity: 0;
    text-align: center;
    -webkit-animation: moveIn 1s 3.1s ease forwards;
    animation: moveIn 1s 3.1s ease forwards;
}
.profile-card header h1 {
    color: #FF5722;
}
.profile-card header a {
    display: inline-block;
    text-align: center;
    position: relative;
    margin: 25px 30px;
}
.profile-card header a:after {
	position: absolute;
    content: "";
	bottom: 3px;
	right: 3px;
	width: 20px;
	height: 20px;
    border: 4px solid #FFFFFF;
    -webkit-transform: scale(0);
    transform: scale(0);
    background: -webkit-linear-gradient(top, #2196F3 0%, #2196F3 50%, #FFC107 50%, #FFC107 100%);
    background: linear-gradient(#2196F3 0%, #2196F3 50%, #FFC107 50%, #FFC107 100%);
    -webkit-border-radius: 50%;
    border-radius: 50%;
    -webkit-box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.1);
    box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.1);
    -webkit-animation: scaleIn 0.3s 3.5s ease forwards;
    animation: scaleIn 0.3s 3.5s ease forwards;
}
.profile-card header a > img {
    width: 120px;
    max-width: 100%;
    -webkit-border-radius: 50%;
    border-radius: 50%;
    -webkit-transition: -webkit-box-shadow 0.3s ease;
    transition: box-shadow 0.3s ease;
    -webkit-box-shadow: 0px 0px 0px 8px rgba(0, 0, 0, 0.06);
    box-shadow: 0px 0px 0px 8px rgba(0, 0, 0, 0.06);
}
.profile-card header a:hover > img {
    -webkit-box-shadow: 0px 0px 0px 12px rgba(0, 0, 0, 0.1);
    box-shadow: 0px 0px 0px 12px rgba(0, 0, 0, 0.1);
}
.profile-card .profile-bio {
    width: 175px;        
    height: 180px;
    display: inline-block;
    float: right;
    padding: 50px 20px 30px 20px;
	background: #FFFFFF;
    color: #333333;
    margin-top: 50px;
    text-align: center;
    opacity: 0;
    -webkit-animation: moveIn 1s 3.1s ease forwards;
    animation: moveIn 1s 3.1s ease forwards;
}
.profile-social-links {
    width: 218px;        
    display: inline-block;
    float: right;
    margin: 0px;
    padding: 15px 20px;
	background: #FFFFFF;
    margin-top: 50px;
    text-align: center;
    opacity: 0;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    -webkit-animation: moveIn 1s 3.1s ease forwards;
    animation: moveIn 1s 3.1s ease forwards;
}
.profile-social-links li {
    list-style: none;
    margin: -5px 0px 0px 0px;
    padding: 0px;
    float: left;
    width: 33.3%;
    text-align: center;
}
.profile-social-links li a {
    display: inline-block;
    width: 24px;
    height: 24px;
    padding: 6px;
    position: relative;
    overflow: hidden!important;
    -webkit-border-radius: 50%;
    border-radius: 50%;
}
.profile-social-links li a img {
    position: relative;
    z-index: 1;
}
.profile-social-links li a:before {
    display: block;
    content: "";
    background: rgba(0, 0, 0, 0.3);
    position: absolute;
    left: 0px;
    top: 0px;
    width: 36px;
    height: 36px;
    opacity: 1;
    -webkit-transition: transform 0.4s ease, opacity 1s ease-out;
    transition: transform 0.4s ease, opacity 1s ease-out;
    -webkit-transform: scale3d(0, 0, 1);
    transform: scale3d(0, 0, 1);
    -webkit-border-radius: 50%;
    border-radius: 50%;
}
.profile-social-links li a:hover:before {
    -webkit-animation: ripple 1s ease forwards;
    animation: ripple 1s ease forwards;
}
.profile-social-links li a img,
.profile-social-links li a svg {
    width: 24px;
}


@media screen and (min-aspect-ratio: 4/3) {
    body {
        background-size: 100% auto;
    }
    body:before {
        width: 0px;
    }
    @-webkit-keyframes puff {
        0% {
            top: 100%;
            width: 0px;
            padding-bottom: 0px;
        }
    	100% {
            top: 50%;
            width: 100%;
            padding-bottom: 100%;
        }	
    }
    @keyframes puff {
        0% {
            top: 100%;
            width: 0px;
            padding-bottom: 0px;
        }
    	100% {
            top: 50%;
            width: 100%;
            padding-bottom: 100%;
        }	
    }
}
@media screen and (min-height: 480px) {
	.profile-card {
		-webkit-animation: init 0.5s 0.2s cubic-bezier(0.55, 0.055, 0.675, 0.19) forwards, moveDown 1s 0.8s cubic-bezier(0.6, -0.28, 0.735, 0.045) forwards, moveUp 1s 1.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards, materia_portrait 0.5s 2.7s cubic-bezier(0.86, 0, 0.07, 1) forwards;
		animation: init 0.5s 0.2s cubic-bezier(0.55, 0.055, 0.675, 0.19) forwards, moveDown 1s 0.8s cubic-bezier(0.6, -0.28, 0.735, 0.045) forwards, moveUp 1s 1.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards, materia_portrait 0.5s 2.7s cubic-bezier(0.86, 0, 0.07, 1) forwards;
	}
	.profile-card header {
        width: auto;
        height: auto;
        padding: 30px 20px;
        display: block;
        float: none;
        border-right: none;
    }
    .profile-card .profile-bio {
        width: auto;
        height: auto;
        padding: 15px 20px 30px 20px;
        display: block;
        float: none; 
    }
    .profile-social-links {
        width: 100%;       
        display: block;
        float: none; 
    }
}
@media screen and (min-aspect-ratio: 4/3) {
    body {
        background-size: 100% auto;
    }
    body:before {
        width: 0px;
		-webkit-animation: puff_landscape 0.5s 1.8s cubic-bezier(0.55, 0.055, 0.675, 0.19) forwards, borderRadius 0.2s 2.3s linear forwards;
		animation: puff_landscape 0.5s 1.8s cubic-bezier(0.55, 0.055, 0.675, 0.19) forwards, borderRadius 0.2s 2.3s linear forwards;
	}
}
@-webkit-keyframes init {
    0% {
    	width: 0px;
    	height: 0px;
    }
	100% {
        width: 56px;
        height: 56px;
        margin-top: 0px;
        opacity: 1;
    }	
}
@keyframes init {
    0% {
    	width: 0px;
    	height: 0px;
    }
	100% {
        width: 56px;
        height: 56px;
        margin-top: 0px;
        opacity: 1;
    }	
}
@-webkit-keyframes puff_portrait {
    0% {
        top: 100%;
        height: 0px;
        padding: 0px;
    }
	100% {
        top: 50%;
        height: 100%;
        padding: 0px 100%;
    }	
}
@keyframes puff_portrait {
    0% {
        top: 100%;
        height: 0px;
        padding: 0px;
    }
	100% {
        top: 50%;
        height: 100%;
        padding: 0px 100%;
    }	
}
@-webkit-keyframes puff_landscape {
	0% {
		top: 100%;
		width: 0px;
		padding-bottom: 0px;
	}
	100% {
		top: 50%;
		width: 100%;
		padding-bottom: 100%;
	}	
}
@keyframes puff_landscape {
	0% {
		top: 100%;
		width: 0px;
		padding-bottom: 0px;
	}
	100% {
		top: 50%;
		width: 100%;
		padding-bottom: 100%;
	}	
}
@-webkit-keyframes borderRadius {
    0% {
        -webkit-border-radius: 50%;
    }
	100% {
        -webkit-border-radius: 0px;
    }	
}
@keyframes borderRadius {
    0% {
        -webkit-border-radius: 50%;
    }
	100% {
        border-radius: 0px;
    }	
}
@-webkit-keyframes moveDown {
    0% {
   	    top: 50%;
    }
	50% {
	   top: 40%;
    }
    100% {
       top: 100%;
    }	
}
@keyframes moveDown {
    0% {
   	    top: 50%;
    }
	50% {
	   top: 40%;
    }
    100% {
       top: 100%;
    }	
}
@-webkit-keyframes moveUp {
    0% {
        background: #FFB300;
        top: 100%;
    }
	50% {
	   top: 40%;
    }
    100% {
       top: 50%;
       background: #E0E0E0;
    }	
}
@keyframes moveUp {
    0% {
        background: #FFB300;
        top: 100%;
    }
	50% {
	   top: 40%;
    }
    100% {
       top: 50%;
       background: #E0E0E0;
    }	
}
@-webkit-keyframes materia_landscape {
    0% {
        background: #E0E0E0;
    }
    50% {
        -webkit-border-radius: 4px;
    }
    100% {
        width: 440px;
        height: 280px;
        background: #FFFFFF;
        -webkit-border-radius: 4px;
    }
}
@keyframes materia_landscape {
    0% {
        background: #E0E0E0;
    }
    50% {
        border-radius: 4px;
    }
    100% {
        width: 440px;
        height: 280px;
        background: #FFFFFF;
        border-radius: 4px;
    }
}
@-webkit-keyframes materia_portrait {
	0% {
		background: #E0E0E0;
	}
	50% {
		-webkit-border-radius: 4px;
	}
	100% {
		width: 280px;
		height: 440px;
		background: #FFFFFF;
		-webkit-border-radius: 4px;
	}
}
@keyframes materia_portrait {
	0% {
		background: #E0E0E0;
	}
	50% {
		border-radius: 4px;
	}
	100% {
		width: 280px;
		height: 440px;
		background: #FFFFFF;
		border-radius: 4px;
	}
}
@-webkit-keyframes moveIn {
    0% {
        margin-top: 50px;
        opacity: 0;
    }
	100% { 
        opacity: 1;
        margin-top: -20px;
    }	
}
@keyframes moveIn {
    0% {
        margin-top: 50px;
        opacity: 0;
    }
	100% { 
        opacity: 1;
        margin-top: -20px;
    }	
}
@-webkit-keyframes scaleIn {
    0% {
        -webkit-transform: scale(0);
    }
	100% { 
        -webkit-transform: scale(1);
    }	
}
@keyframes scaleIn {
    0% {
        transform: scale(0);
    }
	100% { 
        transform: scale(1);
    }	
}
@-webkit-keyframes ripple {
    0% {
        transform: scale3d(0, 0, 0); 
    }
    50%, 100% {
        -webkit-transform: scale3d(1, 1, 1);
    }
    100% {
        opacity: 0;
    }
}
@keyframes ripple {
    0% {
        transform: scale3d(0, 0, 0); 
    }
    50%, 100% {
        transform: scale3d(1, 1, 1);
    }
    100% {
        opacity: 0;
    }
}
</style>

<!--*### Hola, Soy [Juan de Dios](https://Juancruzd.github.io/) <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="25px">
-->
Soy Desarrollador de software, diseño aplicaciones web, android entre otras cosas mas.*
<!--
**Ratheshprabakar/Ratheshprabakar** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
-->

![](https://komarev.com/ghpvc/?username=Juancruzd&color=brightgreen&style=flat)

- 🔭 &nbsp;&nbsp; Actualmente estoy trabajando en [Covid-19 México](https://juancruzd.github.io/mexicovid19/).
- 🌱 &nbsp;&nbsp; Actualmente estoy tratando de aprender [Android](https://developer.android.com/). 
- 📫 Como llegar a mi **juan.cruzd1@outlook.es**
- ⚡ Dato curioso: paso casi 2 horas navegando en Internet todos los días. ¡Me encanta mantenerme actualizado!
 

### Yo en Internet:

[<img align="left" alt="Juancruzd.github.io" width="22px" src="https://raw.githubusercontent.com/iconic/open-iconic/master/svg/globe.svg" />][website]
[<img align="left" alt="shashank | Twitter" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/twitter.svg" />][twitter]
[<img align="left" alt="shashank | LinkedIn" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />][linkedin]
[<img align="left" alt="shashank | Instagram" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/instagram.svg" />][instagram]

<br />
<br />


## &#x1f4c8; Estadísticas de GitHub

<a href="https://github.com/Juancruzd/Juancruzd">
  <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Juancruzd&hide=java,html&title_color=ffffff&text_color=c9cacc&icon_color=2bbc8a&bg_color=1d1f21" />
</a>
<a href="https://github.com/Juancruzd/Juancruzd">
  <img align="center" src="https://github-readme-stats.vercel.app/api?username=Juancruzd&show_icons=true&line_height=27&count_private=true&title_color=ffffff&text_color=c9cacc&icon_color=2bbc8a&bg_color=1d1f21" alt="Juancruzd Estadísticas de GitHub" />
</a>


### Pila de tecnología:

[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/android.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/java.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/kotlin.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/gradle.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/flutter.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/dart.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/jekyll.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/hugo.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/git.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/python.svg" />][website]
[<img align="left" alt="shashank | pub" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/figma.svg" />][website]

[website]: Juancruzd.github.io
[twitter]: https://twitter.com/Juancruzd1_
[instagram]: https://www.instagram.com/Juancruzd1_/
[linkedin]: https://www.linkedin.com/in/juan-de-dios-guadalupe-cruz-delgado/
