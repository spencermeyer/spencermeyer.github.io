---
layout: post
title:  "EnigmaEmulator"
date:   2017-09-11 15:00:00
categories: jekyll update
---

# An Enigma Emulator Application using Rails 5 and React JS

This is an emulator of the enigma coding machine.

There is a React JS front end that provides the keyboard and lampboard, and listens for clicks and sends the click data to the back end.  I've used separate React components for the whole machine, the lampboard, each lamp, the keyboard, and each key.

There is a ruby back end that emulates the rotors.  It listens for the AJAX calls from the front end and provides the logic of the letter transformation throught the rotors, and the rotor rotation, then replies to the AJAX call with the lamp board letter to be lit up on the front end.

[It is hosted here](https://lit-tundra-09860.herokuapp.com/)

<div style="text-align: center">
  <img src='/assets/enigma-machine.png' width='400px'>
</div>
