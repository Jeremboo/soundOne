# SoundOne.js

- [README in French](READMEfr.md)


Simple javascript library to launch a sound. Convenient for sound effects. It is also possible to change the gain and frequency of the sound played . A unique sound can be used several times.

## A personnal script

Create this library was interesting because it is dedicated to doing simple things with the audio API javascript. 

This is a good compromise to avoid using JS libraries largest and most complex.


# Getting started

        var aSound = new SoundOne("my_sound.mp3");
        aSound.play();

Each sound is directly loaded in a 'arrayBuffer' via a XMLHttpRequest object. 

When using the method ``play()``, a contextBuffer object is created and played.

 A chaque lancement de la méthode 'play()', un object contextBuffer est crée et joué. Thus, a single SoundOne object can simultaneously playing a sound loaded.

 A URL can also be passed at the method play() to play directly a new sound :

        aSound.play("my_second_sound.mp3");

Il est tout de même possible de charger un son en amont avec la méthode load();

        aSound.load("my_third_sound.mp3");

# How modified a sound ?

- Change the volume ( 0 has 1) :

        aSound.modifVolume(0.5);

- Change the frequency :

        aSound.modifPlaybackRate(0.8);

Changing the frequency also changes the amount of sound.

## Des choses à redire ?