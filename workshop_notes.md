- [Structure](#structure)
  - [14:00 - 15:30: Input + Hello World](#1400---1530-input--hello-world)
  - [15:30 - 16:00: Input](#1530---1600-input)
  - [16:00 - 16:45: Hands-On](#1600---1645-hands-on)
  - [16:45 - 17:00: Outro](#1645---1700-outro)
- [What is Spark AR?](#what-is-spark-ar)
  - [Why to use](#why-to-use)
  - [What's possible](#whats-possible)
  - [Setup](#setup)
    - [Spark AR Studio](#spark-ar-studio)
    - [Spark AR player on device](#spark-ar-player-on-device)
  - [Limitations](#limitations)
- [Using Spark AR](#using-spark-ar)
  - [Startup Screen](#startup-screen)
  - [Interface](#interface)
    - [Viewport](#viewport)
    - [Scene](#scene)
    - [Asset Manager](#asset-manager)
    - [Patch Editor](#patch-editor)
  - [Building Blocks](#building-blocks)
    - [3D / 2D objects](#3d--2d-objects)
    - [Lights](#lights)
    - [Particle Systems](#particle-systems)
    - [Audio playback](#audio-playback)
    - [Scene Understanding](#scene-understanding)
    - [Scene Extraction](#scene-extraction)
  - [Logic](#logic)
    - [Triggers](#triggers)
    - [Transitions](#transitions)
- [Testing](#testing)
  - [Preview window](#preview-window)
  - [Exporting to Spark AR player](#exporting-to-spark-ar-player)
  - [Exporting to Instagram / Facebook](#exporting-to-instagram--facebook)
- [First Hello World](#first-hello-world)
  - ["Hello World" as text pinned to the head](#hello-world-as-text-pinned-to-the-head)
  - [Transitioning it in](#transitioning-it-in)
  - [Adding cool Facetats](#adding-cool-facetats)
- [3D objects and materials](#3d-objects-and-materials)
  - [Blender toolkit](#blender-toolkit)
  - [ORM texturing (PBR with seperated channels)](#orm-texturing-pbr-with-seperated-channels)
- [Target tracking](#target-tracking)
- [Publishing](#publishing)
  - [Requirements](#requirements)
  - [Spark AR hub](#spark-ar-hub)
- [LEFT OUT:](#left-out)
  - [Segmentation](#segmentation)
  - [Audio playback](#audio-playback-1)
  - [Particles](#particles)
  - [Render pipeline](#render-pipeline)
  - [LUTs](#luts)
  - [Shader](#shader)
    - [Differences from SparkSL to GLSL](#differences-from-sparksl-to-glsl)
  - [Scripting API](#scripting-api)

# Structure

## 14:00 - 15:30: Input + Hello World

## 15:30 - 16:00: Input

## 16:00 - 16:45: Hands-On

## 16:45 - 17:00: Outro

* You will be able to send eachother your first effects at the end!


# What is Spark AR?

* Software to create various augmented reality effect capable of accessing and sharing through Facebook and Instagram
  * Exposes tracking algorithms and render pipeline
  * Creator-friendly framework for artists and programmers of all skill levels
* Started as "Camera Effects Platform" for and by Facebook in April 2017
* Rebranded into "Spark AR" with expansion to Instagram in Oktober 2018

## Why to use

* Less heavy-lifting
  * We _could_ spend hours to code face recognition algorithms and tracking of features and envivronments ourselves
  * _OR:_ We can use a framework that is supported and maintained in the forseeable future by a large group of developers at one of the biggest tech companies in the world
* Track faces, hands, bodies and targets; segment people and hair; place objects in the real world and much more
* Completely free
  * Of course not open source, but you're free to use and publish everything within the guidelines
  * BUT MEH FACEBOOK!
* Facebook (or _✨Meta✨_) sucks, but their products are the ones most used in the world
  * Your experiences are easy to access for most of people
    * No need to download an app
  * The community of Spark AR creators is really big and help is around every corner
  * Constant updates and new features because Facebook is scared of TikTok and its filters!

## What's possible

* 5 filters by me

## Setup

### Spark AR Studio

* Software to create AR effects
* Download under https://sparkar.facebook.com/ar-studio/download/

### Spark AR player on device

* App for devices to test AR effects and quickly access different transferred experiences
* Download in the respective app stores for Android and Apple devices
* Alternatively effects can also be tested directly on the target plattform (You'll need to connect your Facebook account to Spark AR studio first)

## Limitations

* NOT made for asset creation, you will need other programs like Photoshop, Blender or VSCode for your custom assets
* Some features are only available for effects published on Facebook
* The .arexport file containing all the zipped original assets needs to be under 40 MB
* The .arfx file containt the effect with compressed assets needs to be ...
  * ... less than 10 MB for Facebook effects
  * ... less than 4 MB for Instagram effects

# Using Spark AR

## Startup Screen

* Different templates to serve as starting point and to dissect

## Interface

### Viewport

### Scene

### Asset Manager

* Useful for checking export sizes and compression of assets

### Patch Editor

## Building Blocks

### 3D / 2D objects

### Lights

* Maximum is 5 light sources + one envivronment light
* Keep in mind: The light is not gonna effect the camera image
  * Just the Spark AR objects!

### Particle Systems

### Audio playback

* Spark AR only accepts audio in .m4a format with ...
  * Sampling rate: 441000Hz
  * Audio channel: Mono
  * Audio codec: AAC or ALAC (not working on Android device)

### Scene Understanding

### Scene Extraction

* Information from device

## Logic

### Triggers

### Transitions

# Testing

## Preview window

## Exporting to Spark AR player

* Known problem: Fully closing the player on device when updating filter

## Exporting to Instagram / Facebook

* Connecting Spark AR to Facebook account

# First Hello World

## "Hello World" as text pinned to the head

## Transitioning it in

## Adding cool Facetats

# 3D objects and materials

## Blender toolkit

## ORM texturing (PBR with seperated channels)

# Target tracking

* Fixed or Movable Target:
  * _Fixed_ means that once the target is recognized, the camera will position the objects there in camera space. It will NOT move when the target moves.
  * _Movable_ means the opposite and recalculates the target's position each frame.
* LIMITED to a single target!

# Publishing

## Requirements

## Spark AR hub

# LEFT OUT:

## Segmentation

## Audio playback

## Particles

## Render pipeline

## LUTs

## Shader

### Differences from SparkSL to GLSL

## Scripting API