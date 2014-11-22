# SoundOne.js

Simple librairie javascript permettant de lancer un son. Pratique pour les bruitages. Il est aussi possible de modifier le gain et la fréquence du son joué. Un unique son peut donc servir plusieurs fois différements. 

## Un script personnel ammené à être amélioré.

SoundOne est une  librairie personnelle. Elle m'a parue pertinante dans le sens ou elle est dédiée à faire des choses simples avec l'API audio de javascript. C'est un bon compromis permettant d'éviter d'utiliser des librairies JS plus importantes et complexes. 

# Getting started

        var aSound = new SoundOne("my_sound.mp3");
        aSound.play();

Lorsque l'on créer une instance de la classe SoundOne, il est possible de charger directement un son comme dans l'exemple. Chaque son est chargé dans un 'arrayBuffer' via un objet XMLHttpRequest. A chaque lancement de la méthode 'play()', un object contextBuffer est crée et joué. Ainsi un seul objet SoundOne permet de jouer simultanément le son de façon superposé. 

Une url peut aussi être envoyée dans la méthode play() permettant de jouer directement un nouveau son :

        aSound.play("my_second_sound.mp3");

Il est tout de même possible de charger un son en amont avec la méthode load();

        aSound.load("my_third_sound.mp3");

# Comment modifier un son ?

- Pour modifier le volume du son (de 0 à 1) :

        aSound.modifVolume(0.5);

- Pour modifier la fréquence du son (entre xx et xx pour que cela reste audible) :

        aSound.modifPlaybackRate(0.8);

Il faut savoir que modifier la fréquence d'un son modifie aussi sa durée. Plus la fréquence serra basse, plus le son serra long.

## Des choses à redire ?

Des conseils à donner pour l'organisation du code ou son optimisation ? Des méthodes à proposer ? Des adaptations à faire ? N'hésitez pas à me contacter via mon adresse mail **jeremi.boulay@gmail.com**. Tout les avis sont bienvenues ! 