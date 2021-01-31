# Funky Unity Shaders
![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/blewert/funky-unity-shaders)

This is a collection of rather funky (and useful) shaders for visual effects in Unity. You can access the shaders in `Assets/shaders/shaders/` and the materials used in the scenes from `Assets/shaders/materials`. The shaders are created for URP & HDRP with ShaderGraph. However I am considering creating some CG variants for non-SRP builds.

## Why, though?
I frequently create a bunch of shaders for VFX in Unity, and I'm sick of copying them from project-to-project. So this repository serves as a public index of reuseable shaders. It also serves the purpose of showing newcomers to shader development some interesting Examples

## What's in the repository?
In the current version, there are a total of **2** shaders. Note that the path mentioned below is relative to `assets/shaders/`. For example, the full working path of the `billow` shader is `assets/shaders/shaders/billow`.

| Name | File | Description | Applications |
| ---- | ---- | ----------- | ------------ |
| Billow | `shaders/billow` | A world-space billowing displacement shader, using Perlin noise. | Rolling clouds, Blobby objects like slime
| Pulsate | `shaders/pulsate` | A sinusoidal pulsating shader which inflates an object via normal displacement and flashes a given colour. | Hit / alert markers on NPCs or objects, things which are about to explode
| Snow | `shaders/snow` | A procedural snow shader which works by comparing `dot(u, n)` where `u` = `vec3(0, 1, 0)` and `n` is the world-space normal. Performs displacement, albedo and emission calculations. | Snow, Slime
| Distance-based | `shaders/distance-based` | A distance-based shader, which applies 1 or 2 subgraphs depending on a given distance to world-pos `vec3`. | Expanding "shockwave" effects, Distanced-based Dissolve 

# GIFs

## Pulsate
A pulsating shader which flashes and displaces over time. Perfect for bombs which are about to explode, or hitmarkers for NPCs.

![Pulsate Shader Example](https://cdn.discordapp.com/attachments/689485748654833682/802567005541761074/2021-01-21_14-02-22.gif)



## Billow
A cloudy, billowing shader using world-space gradient noise. Very good for rolling clouds and small low-poly puffs of smoke (e.g. when something's hit, or explosions).

![Billow Shader Example](https://cdn.discordapp.com/attachments/689485748654833682/802964512272678963/2021-01-24_18-13-29.gif)


## Snow
A shader which adds snow procedurally using a bit of cool vector math. Good for adding snow or coating objects with a thick viscous layer of something (like slime or acid!).

![Snow Shader Example](https://cdn.discordapp.com/attachments/689485748654833682/802972557719371776/2021-01-24_18-45-48.gif)

## Distance-based
A shader which applies 1 of 2 effects, given the distance to a specific world position (passed as a uniform). In this example, the first effect is render with a normal colour (the red portion) and the second effect is to not render at all (alpha = 0). Based on the distance, the given effect is chosen. To edit the two effects, see the two subgraphs in the folder for this shader.

![Distance-based Shader Example](https://cdn.discordapp.com/attachments/689485748654833682/805475467451695154/2021-01-31_16-30-57.gif)