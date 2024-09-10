---
title: Star Sweepers
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/lZYfTkcNLX4?si=NVE54KEN2VGyObMg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Star Sweepers

- **Developed:** 2023
- **Genre:** Some sort of chill movement

### Overview
Star Sweepers is a movement based game about dodging obstacles and solving objectives around a map. In the game you play as a janitor who sweeps up broken stars in the sky; putting them back together. All while dodging asteroids and aiming for the best time to claim that gold medal.

### What I Did
I was in charge of the majority of gameplay tasks within the project Most notably; the player movement which I am quite happy with. 

[gif of movement]

The movement required constant work during development, changing every week to reflect player feedback to make sure that it was as good as possible since it was the main draw of the game.

The game features two obstacles, both in forms of asteroids that crash down on you while you play. One of these I made.

[gif of asteroid]

This asteroid comes crashing down from an angle and then rolls once it hits the ground. Bouncing of walls and being a general menace.

During development, we used the plugin DoTween which made it easy to animate things through code. For example, the asteroid bounce shown in previous gif was made by tweening. but also this level intro that plays at the start of a level to show where the pieces of the star are located on the map.

[gif of level intro]


### Coding Examples

The actual code for the movement is quite simple. In fact, it is just a smooth and fast version of tank controls 

This is the input code which runs in Update, one notable thing is that the turnspeed is higher when the player is not holding down the acceleration button. This allows for players either to focus on gaining speed or opting for a higher degree of control and precision.

![This is a image!](https://i.ibb.co/1bB5PcB/carbon-1.png "Movement Update Code")

Then for the actual movement of the character; I used a scene object called DirectionMarker. Which just faces direction of movement. I opted to set the velocity instead of using addforce to gain a greater amount of control during development. I also did not need to use the built-in functionality of wall bounces and knockback. 



For the project I also made a sound manager since I am not a big fan of Unitys need of having sound sources on every object that needs to play a sound. It is based on the Sound Manager made by the YouTuber CodeMonkey however I made some changes to better performance.

[pic of sfx manager]

With this, you can call SoundManager.Instance.PlaySound(SoundManager.Sound); In any script at any time to play a sound. The Sounds themself are pooled from a fixed amount of objects that are initialized when game first is loaded. 
I plan on expanding this for future projects and add functionality of setting sound and pitch within the function but also spatial positioning.
