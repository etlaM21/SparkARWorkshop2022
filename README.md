# Spark AR Workshop 2022

This repository functions as a hub with information for you to look up when working with Spark AR and also contains all the materials used in the workshop held on the 25th of February 2022.

Everything here refers to the workings of **Spark AR v129** and won't be updated to ensure validty with future versions of Spark AR.

- [Spark AR Workshop 2022](#spark-ar-workshop-2022)
  - [Setup](#setup)
  - [Useful Ressources](#useful-ressources)

## Setup

You will find the **current version of Spark AR** here: [sparkar.facebook.com/ar-studio/download](https://sparkar.facebook.com/ar-studio/download/)

For testing AR experiences without the need to upload them to the Spark AR hub (to test in Instagram / Facebook), you can use the **Spark AR player** on your device. Find the current version in the respective app store or follow the links on the [official download page](https://sparkar.facebook.com/ar-studio/download/).

Official **assets for face filter** creation can be found here: [lookaside.facebook.com/developers/resources/?id=Face-reference-assets-classic.zip](https://lookaside.facebook.com/developers/resources/?id=Face-reference-assets-classic.zip)

_(Should the link to the assets be moved in the future, you might find the new one in [this page of the documentation](https://sparkar.facebook.com/ar-studio/learn/articles/people-tracking/face-reference-assets))_

## Useful Ressources

**Image compression**: [tinypng.com](https://tinypng.com/)

TinyPNG uses smart lossy compression techniques to reduce the file size of your PNG files

**Convert Audio to .m4a**: [audio.online-convert.com](https://audio.online-convert.com/convert-to-m4a)

Spark AR only accepts audio with .m4a as file format.
[Parameters to use](https://sparkar.facebook.com/ar-studio/learn/articles/fundamentals/supported-file-formats) when converting to .m4a:
- Sampling rate: 441000Hz
- Audio channel: Mono
- Audio codec: AAC (recommendation) or ALAC (not working on Android device)

**Alternatively you can convert your audio using [FFmpeg](https://ffmpeg.org/)**

> ffmpeg -i "your_current_audio.mp3" -y -codec:a libvo_aacenc -ac 1 -ar 44100 -ab 256k "your_new_audio.mp4"

**Ressources shared by the Spark AR community**: [github.com/Spark-AR-Community](https://github.com/Spark-AR-Community)

**Lots of information about and examples of shaders written in SparkSL**: [github.com/aferriss/sparksl-shader-examples](https://github.com/aferriss/sparksl-shader-examples)