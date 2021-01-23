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


## GIFs

### Pulsate
![Pulsate Shader Example](https://cdn.discordapp.com/attachments/689485748654833682/802567005541761074/2021-01-21_14-02-22.gif)