---
layout: project
title: Blindsight: War of the Wardens
date: 2023-05-12
image: /assets/projects/blindsight/header.png
description: A 3D story-driven Brawler
---
## Overview

Blindsight: War of the Wardens is a 3D Brawler I worked on as a tech artist alongside students through USC Games.

[Steam Link](https://store.steampowered.com/app/2187370/Blindsight_War_of_the_Wardens/)

## My Role

While the project originally had a primary tech artist, they had to leave the project and I joined partway through development to add additional polish and potentially create a post release update.

## UI Animations

### Ki Meter 
<div class="video-grid">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/blindsight/meter.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/blindsight/ultimate.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/blindsight/ultimateFinal.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/blindsight/uiFinal.mp4' | relative_url }}" type="video/mp4">
    </video>    
</div>

The player character builds up power and when the meters are filled there would be an effect to indicate that it can be used for stronger attacks. 
After playing around with different looks I settled on A slow pulsing cracked ring that ripples and fades as it expands outwards. I was trying to invoke the feeling of a beating heart but also some kind of magical aura. Alongside the ring there are a few meters that I programmed with some warped noise to add a level of fluid motion to these UI elements.


### Finisher Display
<div class="video-grid">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/blindsight/finisher1.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/blindsight/finisher2.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/blindsight/finisherFinal.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
![programmer art of possible designs](/assets/projects/blindsight/finisher.png)
When designing this effect I wanted it to feel organic and dangerous. It would display when you are able to do a deadly finishing move so I played around with a couple of styles, mixing noise and textures to simulate fire or organic noise. I settled on reusing the texture I had for the Ki meter as it gave the most "Fractured" look.

### Visibility Shader
There were post-release updates planned that would include a revamped visibility shader. Unfortunately that update never got pushed to the published release but I still have files from when I was developing it. 

<div class="video-grid">
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/blindsight/visibility1.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/visibility2.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/visibility3.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/visibility4.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/visibility5.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ '/assets/projects/bloobo/visibility6.mp4' | relative_url }}" type="video/mp4">
    </video>
    <video autoplay muted loop playsinline preload="metadata">
        <source src="{{ 'visibilityShader.png.mp4' | relative_url }}" type="video/mp4">
    </video>
</div>
![programmer art describing the effect design](/assets/projects/bloobo/visibility.png)
![programmer art describing the effect design](/assets/projects/bloobo/visibilityShader.png)
As with many of my vfx additions, I designed it to be modular as possible. The more properties that are accessible to me, the easier it is to tweak.

![Gameplay screenshot](/assets/projects/blindsight/shadergraph.png)
If it doesn't require explicit HLSL I prefer to work in shadergraph because I work best visually and it's helpful to view the individual effects of functions on the shader.