AnimationTP1
============

TP1 Cours d'animation

Cette librairie compte 5 animations différentes, lesquelles peuvent être utilisées de façon individuelle ou collective.

Voici les 5 animations

1- Tourbillon
2- Ping-Pong
3- Métronome
4- Flip
5- Bondir


Ces animations peuvent être utilisées soit avec une forme, du texte ou une image. Attention de ne pas changer les propriétés
des keyframes car cela pourrait avoir un impact sur l'animation qui ne serait plus celle projetée par le code original. 
Par contre, il vous est possible de modifier les propriétés de couleurs à l'intérieur des keyframes. Les propriétés css peuvent
aussi être changé à votre guise dans le document css, tant que cela n'empiète pas sur les autres animations incluses dans cette 
librairie. Vous pouvez aussi modifiez les propriétés des animations en ce qui concerne le nom, la duration, itération-count et 
le timing-function. Vous trouverez de plus amples informations à ce sujet plus bas dans ce document.

Voici la configuration HTML requise.

<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>Animation</title>
<link rel="stylesheet" type="text/css" href="style.css">
<script type="text/javascript" src="prefixfree.min.js"></script>
</head>

<body>

	<!-- ANIMATION TOURBILLON-->
	<div class= "tourbillon">
</div>
    
    <!-- ANIMATION PING-PONG-->	
    <div class= "pingpong">
</div>
   
     
        <!-- ANIMATION METRONOME-->	
    <div class="metronome">
</div>
    
     <!-- ANIMATION flip-->	
    <div class="flip">
</div>
    
    
        <!-- ANIMATION BONDIR-->	
    <div class="bondir">
</div>   

</body>
</html>


Ne pas oublier de joindre le fichier prefixfree.min.js que vous pouvez télécharger au lien suivant.

http://leaverou.github.io/prefixfree/




LES DIFFÉRENTES ANIMATIONS DE LA LIBRAIRIES.


1- ANIMATION TOURBILLON

Cette animation à pour but de représenter un effet tourbillon en vas et viens.

Vous aurez besoin de vous créer une balise div avec une classe .tourbillon que l'animation puisse fonctionner.
Si vous utiliser du texte vous devrez avec une balise de type p, h1 ou autre et l'inscrire dans votre css ou une
balise img pour une image. N'oubliez pas de les insérer dans votre css pour que le tout puisse fonctionner.
(Ex: .tourbillon p{) pour une balise p de texte.

Les paramètres ci-dessous sont modifiables dans le fichier style.css.

Vous pouvez dans cette animation changer quelques petites choses.


.tourbillon{ 

	(vous pouvez changer le nom de la classe ou l'id par ce que vous désirez)

	display: inline-block; (Vous pouvez changer le type de display en display: block par exemple)
	width: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
	height: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image
	margin-top: 350px; (La position peut aussi être modifié comme vous le désirez)
	margin-left: 500px; (La position peut aussi être modifiée comme vous le désirez)
	margin-right: 50px; (La position peut aussi être modifiée comme vous le désirez)
	background: red; (La couleur peut être conservé ou retiré complètement dépendamment de l'utilisation que vous en faites)
	border-radius: 10px; (Ceci arrondit les coins de la forme, cela peut être conservé ou retiré complètement aussi)


/* Navigateur Internet Explorer version 10 et +.  */

	animation-name: tourbillon; /* Nom de l'animation. */
	animation-duration: 2s; /* Nombre de temps que l'animation sera exécutée. */
	animation-iteration-count: infinite; /* Nombre de fois que l'animation sera exécutée. */
	animation-timing-function: ease; /* Spécifie la vitesse de la courbe de l'animation.*/


Voici pour ce qui peut être modifié dans cette animation. Les données doivent être 
identique dans tous les keyframes et animation si l'on veut retrouver la même animation dans  tous les navigateurs.

animation-name: tourbillon; 
Ici il vous est permis de changer le nom de l'animation. (Ne pas oublier de le changer dans le Keyframes aussi.)

animation-duration: 2s;
Ici vous pouvez changer le temps en seconde (ex:1s) de la durée pendant laquelle l'animation sera exécutée.
Plus le temps est court plus l'animation se déroule rapidement, plus le temps est long plus l'animation ce déroule lentement.


animation-iteration-count: infinite; 
Ici vous pouvez changer le nombre de fois que l'animation sera exécutée. Vous pouvez le représenter par un nombre (ex:50 qui veut
dire que l'animation va recommencer 50 fois) ou y inscrire infinite qui veut dire que l'animation va recommencer à l'infini.

animation-timing-function: ease; 
Ici vous pouvez spécifier la vitesse de la courbe de l'animation. Par ease, ease-in, ease-out, ease-in-out, linear ou encore le cube de
bézier.

ease: décélère légèrement au début et termine sa transition lentement.
ease-in: commencera lentement.
ease-in-out: commencera et finira lentement.
linear: la transition sera stable sans décélération ni accélération.
cubic-bezier: (0, 0, 0, 0) cela défini la courbe de l'animation.


Vous pouvez aussi changer les différentes informations dans les keyframes qui sont reliés à l'opacité ou la couleur quand elles
sont appliquées, mais évité de changer les propriétés transform ou animation car cela changerait les propriétés originales de l'animation
et ce quelle projette. Il vous est quand même possible d'expérimenter les pourcentages de début et de fin de l'animation, mais cela changera
l'animation.

/* Navigateur Internet Explorer version 10 et +.  */


@keyframes tourbillon {ici il vous est permis de changer le nom du keyframe. (Ne pas oublier de le changer dans l'animation aussi.)

	0%	{	
		background-color: black;
		transform: rotate(0deg) scale(1) skew(1deg) translate(10px);
		}
	50%	{
		background-color: red;
		transform: rotate(365deg) scale(0.250) skew(-28deg) translate(-15px); 
		}
	100%{
		background-color: black;
		transform: rotate(0deg) scale(1) skew(1deg) translate(10px);
		}
} 






2- ANIMATION PING-PONG

Cette animation a pour but de représenter un effet de mouvement qui s'apparente à celui d'une balle de ping-pong en action.


Les paramètres ci-dessous sont modifiables dans le fichier style.css.

Vous pouvez dans cette animation changer quelques petites choses.


.pingpong{ 
	(vous pouvez changer le nom de la classe ou l'id par ce que vous désirez)

	height: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
	width: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
	border-radius: 100%; (Ceci arrondit les coins de la forme, cela peut être conservé ou retiré complètement aussi.)
	background-color: red; (La couleur peut être conservée ou retirée complètement dépendamment de l'utilisation que vous en faites)
	display: inline-block; (Vous pouvez changer le type de display en display: block par exemple)
	margin-right: 50px; (La position peut aussi être modifiée comme vous le désirez)



/* Navigateur Internet Explorer version 10 et +.  */

	animation-name: pingpong;  /* Nom de l'animation. */
	animation-duration: 5s;  /* Nombre de temps que l'animation sera exécutée. */
	animation-iteration-count: 3;  /* Nombre de fois que l'animation sera exécutée. */
	animation-timing-function: ease-in-out; /* Spécifie la vitesse de la courbe de l'animation.*/
	animation-delay: 1s; /* Spécifie dans combien de temps l'animation débutera */


Voici pour ce qui peut être modifié dans cette animation. Les données doivent être 
identique dans tous les keyframes et animation si l'on veut retrouver la même animation dans  tous les navigateurs.

animation-name: pinpong; 
Ici il vous est permis de changer le nom de l'animation. (Ne pas oublier de le changer dans le Keyframes aussi.)

animation-duration: 5s;
Ici vous pouvez changer le temps en seconde(ex:1s) de la durée pendant laquelle l'animation sera exécutée.
Plus le temps est court plus l'animation ce déroule rapidement, plus le temps est long plus l'animation ce déroule lentement.


animation-iteration-count: 3; 
Ici vous pouvez changer le nombre de fois que l'animation sera exécutée. Vous pouvez le représenter par un nombre(ex:50 qui veut
dire que l'animation va recommencer 50 fois) ou y inscrire infinite qui veut dire que l'animation va recommencer à l'infini.

animation-timing-function: ease-in-out; 
Ici vous pouvez spécifier la vitesse de la courbe de l'animation. Par ease, ease-in, ease-out, ease-in-out, linear ou encore le cube de
bézier.

ease: décélère légèrement au début et termine sa transition lentement.
ease-in: commencera lentement.
ease-in-out: commencera et finira lentement.
linear: la transition sera stable sans décélération ni accélération.
cubic-bezier: (0, 0, 0, 0) cela défini la courbe de l'animation.

animation-delay: 1s; 
Ici vous pouvez changer le temps en seconde(ex:1s) et cela déterminera le délai avant que l'animation débute.


Vous pouvez aussi changer les différentes informations dans les keyframes qui sont reliés à l'opacité ou la couleur quand elles
sont appliquées, mais évité de changer les propriétés transform ou animation car cela changerait les propriétés originales de l'animation
et ce quelle projette. Il vous est quand même possible d'expérimenter les pourcentages de début et de fin de l'animation, mais cela changera
l'animation. 


/* Navigateur Internet Explorer version 10 et +.  */

@keyframes pingpong{
	
	0%{ 
		background-color: blue;
		transform: scalex(1) translate(0px);
	}	 
	50%{
		background-color: yellow;
		transform: scalex(-1)  translate(30px);
	}	
	100%{
		background-color: blue;
		transform: scalex(1)  translate(0px);
	}
}






3- ANIMATION METRONOME

Cette animation à pour but de représenter un effet de mouvement qui s'apparente à celui d'un métronome.


Les paramètres ci-dessous sont modifiables dans le fichier style.css.

Vous pouvez dans cette animation changer quelques petites choses.


.metronome{
	(vous pouvez changer le nom de la classe ou l'id par ce que vous désirez)
	
	display: inline-block; (Vous pouvez changer le type de display en display: block par exemple)
	width: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
	height: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
	background: red; (La couleur peut être conservé ou retiré complètement dépendamment de l'utilisation que vous en faites)
	border-radius: 10px; (Ceci arrondi les coins de la forme, cela peut être conservé ou retiré complètement aussi.)
	margin-right: 50px; (La position peut aussi être modifiée comme vous le désirez)

	
/* Navigateur Internet Explorer version 10 et +.  */

 	animation-name: metronome; /* Nom de l'animation. */
        animation-duration: 1s; /* Nombre de temps que l'animation sera exécutée. */
	animation-iteration-count: 8; /* Nombre de fois que l'animation sera exécutée. */
	animation-timing-function: ease; /* Spécifie la vitesse de la courbe de l'animation.*/
	animation-delay: 2s; /* Spécifie dans combien de temps l'animation débutera */


Voici pour ce qui peut être modifié dans cette animation. Les données doivent être 
identique dans tous les keyframes et animation si l'on veut retrouver la même animation dans  tous les navigateurs.

animation-name: metronome; 
Ici il vous est permis de changer le nom de l'animation. (Ne pas oublier de le changer dans le Keyframes aussi.)

animation-duration: 1s;
Ici vous pouvez changer le temps en seconde(ex:1s) de la durée pendant laquelle l'animation sera exécutée.
Plus le temps est court plus l'animation ce déroule rapidement, plus le temps est long plus l'animation ce déroule lentement.


animation-iteration-count: 8; 
Ici vous pouvez changer le nombre de fois que l'animation sera exécutée. Vous pouvez le représenter par un nombre(ex:50 qui veut
dire que l'animation va recommencer 50 fois) ou y inscrire infinite qui veut dire que l'animation va recommencer à l'infini.

animation-timing-function: ease; 
Ici vous pouvez spécifier la vitesse de la courbe de l'animation. Par ease, ease-in, ease-out, ease-in-out, linear ou encore le cube de
bézier.

ease: décélère légèrement au début et termine sa transition lentement.
ease-in: commencera lentement.
ease-in-out: commencera et finira lentement.
linear: la transition sera stable sans décélération ni accélération.
cubic-bezier: (0, 0, 0, 0) cela défini la courbe de l'animation.

animation-delay: 2s; 
Ici vous pouvez changer le temps en seconde(ex:1s) et cela déterminera le délai avant que l'animation débute.


Vous pouvez aussi changer les différentes informations dans les keyframes qui sont reliés à l'opacité ou la couleur quand elles
sont appliquées, mais évité de changer les propriétés transform ou animation car cela changerait les propriétés originales de l'animation
et ce quelle projette. Il vous est quand même possible d'expérimenter les pourcentages de début et de fin de l'animation, mais cela changera
l'animation.


/* Navigateur Internet Explorer version 10 et +.  */

@keyframes metronome{
	0%{ 
		transform: scale(1) skew(-10deg);
		opacity: 1.0;
		background-color: red;
	}
	50%{
		transform: scale(-1);
		opacity: 0.5;
		background-color: yellow;
		
	}
	100%{
		transform: scale(1) skew(-10deg);
		opacity: 1.0;	
		background-color: green;
	}	
}





4- ANIMATION FLIP

Cette animation à pour but de représenter un effet de mouvement qui s'apparente à tableau ou l'on peut retourner des lettres par exemple.


Les paramètres ci-dessous sont modifiables dans le fichier style.css.

Vous pouvez dans cette animation changer quelques petites choses.


.flip{ 
	(vous pouvez changer le nom de la classe ou l'id par ce que vous désirez)
	display: inline-block; (Vous pouvez changer le type de display en display: block par exemple)
	width: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
	height: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
	background: red; (La couleur peut être conservé ou retiré complètement dépendamment de l'utilisation que vous en faites)
	border-radius: 10px; (Ceci arrondi les coins de la forme, cela peut être conservé ou retiré complètement aussi.)
	margin-right: 50px; (La position peut aussi être modifiée comme vous le désirez)

	
/* Navigateur Internet Explorer version 10 et +.  */

 	animation-name: flip; /* Nom de l'animation. */
        animation-duration: 7s; /* Nombre de temps que l'animation sera exécutée. */
	animation-iteration-count: 4; /* Nombre de fois que l'animation sera exécutée. */
	animation-timing-function: ease; /* Spécifie la vitesse de la courbe de l'animation.*/
	animation-delay: 2s; /* Spécifie dans combien de temps l'animation débutera */


Voici pour ce qui peut être modifié dans cette animation. Les données doivent être 
identique dans tous les keyframes et animation si l'on veut retrouver la même animation dans  tous les navigateurs.

animation-name: flip; 
Ici il vous est permis de changer le nom de l'animation. (Ne pas oublier de le changer dans le Keyframes aussi.)

animation-duration: 7s;
Ici vous pouvez changer le temps en seconde(ex:1s) de la durée pendant laquelle l'animation sera exécutée.
Plus le temps est court plus l'animation ce déroule rapidement, plus le temps est long plus l'animation ce déroule lentement.


animation-iteration-count: 4; 
Ici vous pouvez changer le nombre de fois que l'animation sera exécutée. Vous pouvez le représenter par un nombre(ex:50 qui veut
dire que l'animation va recommencer 50 fois) ou y inscrire infinite qui veut dire que l'animation va recommencer à l'infini.

animation-timing-function: ease; 
Ici vous pouvez spécifier la vitesse de la courbe de l'animation. Par ease, ease-in, ease-out, ease-in-out, linear ou encore le cube de
bézier.

ease: décélère légèrement au début et termine sa transition lentement.
ease-in: commencera lentement.
ease-in-out: commencera et finira lentement.
linear: la transition sera stable sans décélération ni accélération.
cubic-bezier: (0, 0, 0, 0) cela défini la courbe de l'animation.

animation-delay: 2s; 
Ici vous pouvez changer le temps en seconde(ex:1s) et cela déterminera le délai avant que l'animation débute.


Vous pouvez aussi changer les différentes informations dans les keyframes qui sont reliés à l'opacité ou la couleur quand elles
sont appliquées, mais évité de changer les propriétés transform ou animation car cela changerait les propriétés originales de l'animation
et ce quelle projette. Il vous est quand même possible d'expérimenter les pourcentages de début et de fin de l'animation, mais cela changera
l'animation.


/* Navigateur Internet Explorer version 10 et +.  */

@keyframes flip{
	0%{ 
		transform: scalex(1) rotatex(0deg);
		background-color: red;
	}	 
	50%{
		transform: scalex(1) rotatex(1800deg);
		background-color: black;
	}	
	100%{
		transform: scalex(1) rotatex(0deg);
		background-color: red;
	}	
}





5- ANIMATION BONDIR

Cette animation a pour but de représenter le mouvement d'une balle qui rebondit au plafond et rebondit dans le chemin inverse.



Les paramètres ci-dessous sont modifiables dans le fichier style.css.

Vous pouvez dans cette animation changer quelques petites choses.



.bondir{
	(vous pouvez changer le nom de la classe ou l'id par ce que vous désirez)

	display: inline-block; (Vous pouvez changer le type de display en display: block par exemple)
	La position: relative; (vous pouvez changer ceci par les différentes positions que voici:
	
	La position absolu : il nous permet de placer un élément n'importe où sur la page (en haut à gauche, en bas à droite, tout au centre, etc.).
	La position fixe : identique au positionnement absolu, mais, cette fois, l'élément reste toujours visible,
        même si on descend plus bas dans la page. C'est un peu le même principe que background-attachment: fixed; (si vous vous en souvenez encore).
	La position relative : permets de décaler l'élément par rapport à sa position normale.


   	width: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
    	height: 40px; (Le format de la forme peut être remplacé par du texte dans une balise appropriée ou une balise image)
	background: red; (La couleur peut être conservé ou retiré complètement dépendamment de l'utilisation que vous en faites)
    	border-radius: 100%; (Ceci arrondi les coins de la forme, cela peut être conservé ou retiré complètement aussi.)
	margin-right: 50px; (La position peut aussi être modifiée comme vous le désirez)
	
	
/* Navigateur Internet Explorer version 10 et +.  */

 	animation-name: bondir; /* Nom de l'animation. */
        animation-duration: 4s; /* Nombre de temps que l'animation sera exécutée. */
	animation-iteration-count: 4; /* Nombre de fois que l'animation sera exécutée. */
	animation-timing-function: ease; /* Spécifie la vitesse de la courbe de l'animation.*/
	animation-delay: 1s; /* Spécifie dans combien de temps l'animation débutera */


Voici pour ce qui peut être modifié dans cette animation. Les données doivent être 
identique dans tous les keyframes et animation si l'on veut retrouver la même animation dans  tous les navigateurs.

animation-name: bondir; 
Ici il vous est permis de changer le nom de l'animation. (Ne pas oublier de le changer dans le Keyframes aussi.)

animation-duration: 4s;
Ici vous pouvez changer le temps en seconde(ex:1s) de la durée pendant laquelle l'animation sera exécutée.
Plus le temps est court plus l'animation ce déroule rapidement, plus le temps est long plus l'animation ce déroule lentement.


animation-iteration-count: 4; 
Ici vous pouvez changer le nombre de fois que l'animation sera exécutée. Vous pouvez le représenter par un nombre(ex:50 qui veut
dire que l'animation va recommencer 50 fois) ou y inscrire infinite qui veut dire que l'animation va recommencer à l'infini.

animation-timing-function: ease; 
Ici vous pouvez spécifier la vitesse de la courbe de l'animation. Par ease, ease-in, ease-out, ease-in-out, linear ou encore le cube de
bézier.

ease: décélère légèrement au début et termine sa transition lentement.
ease-in: commencera lentement.
ease-in-out: commencera et finira lentement.
linear: la transition sera stable sans décélération ni accélération.
cubic-bezier: (0, 0, 0, 0) cela défini la courbe de l'animation.

animation-delay: 1s; 
Ici vous pouvez changer le temps en seconde(ex:1s) et cela déterminera le délai avant que l'animation débute.


Vous pouvez aussi changer les différentes informations dans les keyframes qui sont reliés à l'opacité ou la couleur quand elles
sont appliquées, mais évité de changer les propriétés transform ou animation car cela changerait les propriétés originales de l'animation
et ce quelle projette. Il vous est quand même possible d'expérimenter les pourcentages de début et de fin de l'animation, mais cela changera
l'animation.


/* Navigateur Internet Explorer version 10 et +.  */

@keyframes bondir{
    0%{
      bottom: 0px;
      animation-timing-function: ease-out;
      transform: translateX(0px);
      background-color: red;	  
    }
    25%{
      bottom: 400px;
      animation-timing-function: ease-in;
      background-color: green;
      transform: translateX(50px);
    }
    50%{
      bottom: 0px;
      animation-timing-function: ease-out;
      background-color: blue; 
      transform: translateX(100px);
    }
    75%{
      bottom: 400px;
      animation-timing-function: ease-in;
      background-color: green;
      transform: translateX(50px);
    }
    100%{
      bottom: 0px;
      animation-timing-function: ease-out;
      background-color: blue; 
      transform: translateX(0px);
    }
 }

