# RealityKit Terrain Shader
This project shows you how to use Fractal Brownian Motion (fBM) to generate an Augmented Reality (AR) Terrain using iOS RealityKit Custom Materials. RealityKit Custom Material includes a surface shader and geometry modifier, also known as fragment and vertex shaders in OpenGL.

<img src=images/realitykit_terrain_shader.gif>

## Fractal Brownian Motion (fBM)

fBM (Fractal Brownian Motion) is used extensively in computer graphics to model natural phenomenons and textures such as terrain , coastline, fire, smoke, clouds, water flow, water waves , rapids, dinosaur skin, wrinkles etc. It is quite amazing to note how such a simple random function can be used in so many areas to emulate the various forms of nature.

This project shows how you can use the fBM function to very simply generate a terrain using iOS RealityKit custom materials (which includes the surface shader and geometry modifier, also known as fragment and vertex shaders in OpenGL)

### Parameters
The form of fBM function we are using has mainly the parameters

uv - texture coordinates (a value of [0,0] to [1,1], representing the four corners of an image we will like to generate)

time - in seconds (this value will animate the fBM generate image with respect to time)

### Properties of the fBM

A fBM can return a single value (one dimensional value) or multiple values (e.g a 3 dimensional vector). You can view a fBM as a random number generator that depends on the current pixel position of the image. However, it is not completely random because the function varies quite smoothly with respect to its neighbours.

So if the user pass in uv-coordinate values of (0.10,0.10) and (0.11,0.10) the returned value should be quite near to each other. For a 3 dimensional vector , the value of each component will be quite similar to its neighbour’s.

Apart from varying smoothly with respect to space (i.e position or uv-coordinates), the fBM also varies quite smoothly with respect to time. So a returned value at time = 0.10 sec will be quite similar to a value at time = 0.11 sec. This gives it the property of having a smooth animation w.r.t. time.

Furthermore, the continuity of many implementations fBM is not restricted to just continuity of values, but also the continuity of its gradient as well as the continuity of (radius of) curvature. This make the fBM function very ‘smooth’ and thus very suitable for artistic renderings.

A fBM has fractal like properties. If you zoom in to small area, you will be able to notice similar patterns when the image has not been zoomed in.

## Detailed Description

[RealityKit Terrain Shader with Surface Shader and Geometry Modifier](https://photorealityar.com/digitalcompositing.html](https://photorealityar.com/realitykit_terrainshader_surfaceshader_geometrymodifier.html))

# Source Code License - GPLv2

RealityKit Terrain Shader
Copyright (C) 2023 djembe-waka 

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

# Compile

### Prerequisites

* Xcode 14
* iOS 16

### Build

* Download the Source Code
* Launch Xcode and load RealityShaders.xcodeproj 
* Build and run on iPhone Simulator or Device

