---
layout: project
title: Bloobo
date: 5/8/2023
image: /assets/projects/bloobo/bloobo_happy.png
description: A short description of my game.
---

## Overview

Bloobo is a 2D Physics based platformer that I worked on as a collaboration with a team of students through USC Games.

<div class="youtube-embed">
    <iframe
        src="https://www.youtube.com/embed/ARLkv1fgV8w"
        title="YouTube video"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen>
    </iframe>
</div>

<div class="image-grid">
    <img src="{{ '/assets/projects/bloobo/bb_screenshot_1' | relative_url }}" alt="Gameplay screenshot 1">
    <img src="{{ '/assets/projects/bloobo/bb_screenshot_2' | relative_url }}" alt="Gameplay screenshot 2">
    <img src="{{ '/assets/projects/bloobo/bb_screenshot_3' | relative_url }}" alt="Gameplay screenshot 3">
    <img src="{{ '/assets/projects/bloobo/bb_screenshot_4' | relative_url }}" alt="Gameplay screenshot 4">
    <img src="{{ '/assets/projects/bloobo/bb_screenshot_5' | relative_url }}" alt="Gameplay screenshot 5">
    <img src="{{ '/assets/projects/bloobo/bb_screenshot_6' | relative_url }}" alt="Gameplay screenshot 6">
    <img src="{{ '/assets/projects/bloobo/bb_screenshot_7' | relative_url }}" alt="Gameplay screenshot 7">
</div>

The game was hosted on the IOS app store but is currently not available.

## My Role

I worked as a Tech Artist and contributed to the game's particle effects and vfx using shaders.

## My Contributions

### Blur Shader and effects derived from it
![visual shadergraph showing a blur shader](/assets/projects/bloobo/blurshader.png)

One of the most widely used tools I created for this game was a blur effect. Effectively I was using a script to apply a custom shader onto any image then store that. It ran once when the GameObject was loaded and created a temporary image file in data so the blur wouldn't have to run every frame at the cost of some ram. Softer and smoother looking blurs are often incredibly costly on a GPU and because this game was designed to run on phones, this was my workaround to keep it performant. 

<div class="image-grid">
    <img src="{{ '/assets/projects/bloobo/blur1' | relative_url }}" alt="blur effect">
    <img src="{{ '/assets/projects/bloobo/blur2' | relative_url }}" alt="blur effect">
    <img src="{{ '/assets/projects/bloobo/blur3' | relative_url }}" alt="blur effect">
</div>

The Blur was originally created to soften background art so it would feel like the player character was microscopic. I could easily tweak the parameters of the shader to create other effects such as a glows. (I was using a temp asset for these because it was an image I had on hand that had a complex alpha)

![discord log showing the blur shader](/assets/projects/bloobo/blurShaderFace.png)
For example; An Inner glow
![discord log showing inner glow](/assets/projects/bloobo/innerGlow.png)
and an Outer Glow
![discord log showing glow](/assets/projects/bloobo/glowShader.png)
![discord log showing glow](/assets/projects/bloobo/glowShader2.png)
These were created with the intention to be used throughout the project but I don't think they were actually used. 
![discord log showing a dotted line effect](/assets/projects/bloobo/dottedLineShader.png)
This was an early version of the trail effect for when selecting objects.

### Old Particles
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/oldParticles.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
This is a close-to-final but not yet final archive of most of the particle effects I had created. The black hole is notable different from the final version.

### Black Hole
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/blackHole.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>

### Portal Particles
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/portalParticles.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
I was proud of this one, these were meant to be eye-catching particles to clue the player that this is something the player wants to collide with.

### select Burst
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/selectBurst.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
One of the minor effects I created for overall UX, to give more player feedback when selecting and moving objects.

### Zoomies
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/zoomies.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
This effect was created to play whenever the player reaches a certain speed and add a touch of gamefeel.

### Click Effect
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/clickEffect.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
More UX and feedback enhancements. This seems complex but it's just an particle effect being scaled with it's opacity being lowered!

### confetti
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/confetti.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
This effect went through lots of revisions until it felt just right. I'm not sure if this is the final version but it's very close. The confetti needed to feel excessive.

### edge Collision
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/edgeCollision.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
I styled this effect after Fox's shine from Super Smash Brothers. I used a lerp to animate through a alpha mask which I multiplied with whatever color I wanted. Many of these effects were made with as much modularity as I could so I could change colors of things whenever we needed.

### Falling Screen Transition
<div class="portfolio-video">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/fallAnim.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
One of the last effects I worked on before it was released, Using a wall of animated particles, this would play when transitioning between levels.