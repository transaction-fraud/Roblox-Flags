---
layout: default
title: Roblox Flags — Complete List of Fast Flags
description: A repository documenting every available allowlisted Roblox fast flag, their default values, and explanations.
---

# Roblox-Flags
![CC0 1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey)

A repository for every single available flag in the allowlist and an explanation of what they do.

###### [If you wish to use these flags, the following bootstrappers are recommended if applicable: Bloxstrap for Windows, Appleblox for MacOS and Sober for Linux. Refer to their websites on how to use flags for their software]
###### [Roblox fast flags are intended only for developers and engineers, there may be flags removed or added at any time to the allowlist. This repository is for educational purposes only, and any usage is at your own risk.]
##### [Only default values are shown here]
### CSG Level of Detail (LOD) Switching Distance
Controls the quality or detail of a mesh at a distance (each level represents a lower quality (L34 being the lowest) and the values define what distance each level activates at).
```text
    "DFIntCSGLevelOfDetailSwitchingDistance": 250,
    "DFIntCSGLevelOfDetailSwitchingDistanceL12": 500,
    "DFIntCSGLevelOfDetailSwitchingDistanceL23": 750,
    "DFIntCSGLevelOfDetailSwitchingDistanceL34": 1000
```

### Handle Alt Enter Manually
By default this is always true, allows you to enter exclusive fullscreen (aka FSE) by pressing alt+enter instead of F11. The primary reason why you might use exclusive fullscreen over borderless as it gives Roblox direct control over the display, bypassing DWM. This has some noticeable performance improvements though it makes alt tabbing much worse and Roblox incompatible with certain overlays.

```text
    "FFlagHandleAltEnterFullscreenManually": true
```

### Texture Quality Override
When ``"DFFlagTextureQualityOverrideEnabled"`` is true, allows the integar flag to work below. The value (for ``"DFIntTextureQualityOverride"``) controls the texture quality level of Roblox, 0 being the lowest quality and 3 being the highest. The effect is similar to the original SkipMips flag, where objects and effects appear blurred or square the lower the value.

```text
    "DFFlagTextureQualityOverrideEnabled": false,
    "DFIntTextureQualityOverride": 3
```

### Force MSAA Samples
Controls the MSAA (Multi-Sample Anti-Aliasing) level, only valid values are 0, 1, 2, 4, 8 (anything higher and it will default back to 8 and anything higher than 4 breaks viewports). This flag dynamically changes depending on the users graphics level so becomes useless when using something that forces it (``"DFIntDebugFRMQualityLevelOverride"``).

```text
    "FIntDebugForceMSAASamples": 0
```

### Disable DPI Scaling
When true, fixes Roblox's rendering quality decreasing when having a display scale greater than 100%.

```text
    "DFFlagDisableDPIScale": false
```

### Prefer DirectX 11
When rendering, prefer the Direct3D 11 API over anything else if set true. In general, most computers using Windows made past 2010 support this, and Roblox would use this as default anyway meaning you are probably already using D3D11 if you are on Windows. Incompatible on MacOS and Linux.
```text
    "FFlagDebugGraphicsPreferD3D11": false
```

### Prefer Vulkan
When true, forces the rendering API to use Vulkan, the successor of OpenGL, unlike D3D11 Vulkan supports MacOS through the MoltenVK translation layer and Linux natively supports it. It is considered to be more performant than D3D11 though it is somewhat less stable with display issues such as HDR incompatibility .

```text
    "FFlagDebugGraphicsPreferVulkan": false
```

### Prefer OpenGL
An older rendering engine, and is often used as a fallback API when the current system does not support D3D11 or Vulkan. Note: MacOS no longer has OpenGL updated on their systems.


```text
    "FFlagDebugGraphicsPreferOpenGL": false
```

### Gray Sky
Sets the sky to be gray, or not. Only works on games that use Roblox's default skybox

```text
    "FFlagDebugSkyGray": false
```

### Pause Voxelizer
When true while using voxel lighting (NO LONGER POSSIBLE USING ALLOWLIST), removes all shadows and lighting. This makes some games far darker or brighter than expected. 

```text
    "DFFlagDebugPauseVoxelizer": false
```

### FRM Quality Override
Controls graphics similarily to the graphics slider in Roblox. Uses the old 21 graphics level values (which is why having value of 1 on this flag is lower quality than the actual first graphics level on the slider). Due to how the graphics setting works also controls the MSAA, SSAO and PostFx levels.

```text
    "DFIntDebugFRMQualityLevelOverride": 0
```

### Min/Max Grass Distance
Controls how short or tall grass can be. Only applies to Roblox's own grass model.

```text
    "FIntFRMMaxGrassDistance": 290,
    "FIntFRMMinGrassDistance": 100
```
There is also this flag that controls grass motion ``"FIntGrassMovementReducedMotionFactor": 5`` which also only applies to Roblox's animated grass model.

# Special Thanks / Sources
Flemish for his [repository](https://github.com/LeventGameing/allowlist/blob/main/allowlist.json) on every allowlist flag

[Roblox Dev Forums](https://devforum.roblox.com)

[Bloxstrap Wiki](https://github.com/bloxstraplabs/bloxstrap/wiki)

###### V1.0.1