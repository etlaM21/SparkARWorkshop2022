# Spark AR Workshop 2022

This repository functions as a hub with information for you to look up when working with Spark AR and also contains all the materials used in the workshop held on the 25th of February 2022.

Everything here refers to the workings of **Spark AR v129** and won't be updated to ensure validty with future versions of Spark AR.

- [Spark AR Workshop 2022](#spark-ar-workshop-2022)
  - [Setup](#setup)
  - [Publishing](#publishing)
    - [Requirements](#requirements)
    - [Making the effect accesable on Instagram / Facebook](#making-the-effect-accesable-on-instagram--facebook)
  - [Problems to look out for](#problems-to-look-out-for)
  - [Useful Ressources](#useful-ressources)
    - [Offical Ressources](#offical-ressources)
    - [Unofficial Ressources](#unofficial-ressources)

## Setup

You will find the **current version of Spark AR** here: [sparkar.facebook.com/ar-studio/download](https://sparkar.facebook.com/ar-studio/download/)

For testing AR experiences without the need to upload them to the Spark AR hub (to test in Instagram / Facebook), you can use the **Spark AR player** on your device. Find the current version in the respective app store or follow the links on the [official download page](https://sparkar.facebook.com/ar-studio/download/).

## Publishing

### Requirements

[File sizes]

[Capabilities]

### Making the effect accesable on Instagram / Facebook

To publish your AR experience on Facebook and/or Instagram you will **need to have a Facebook account**.

1. Export your effect out of Spark AR by opening the publish menu. You can **export the effect** or directly upload it to the Spark AR Hub should you logged in your Facebook in Spark AR already. _Then you can skip ahead to step 3_.
2. **Go to the** [**Spark AR Hub**](https://www.facebook.com/sparkarhub/dashboard) and login to the Facebook on which you want to publish your project. For Instagram experiences this means you need to choose the account which the Instagram account is linked to.
3. On the **button "Publish Effect"** you can fill out all the needed information about your filter and also upload the .arexport file you got out of Spark AR. _Important note: If you choose Facebook only as your target plattform, you can't change it afterwards. You have to delete your effect and start the process over._
4. You will now need a preview image and video for your experience. Click **save and then send yourself a test link to the target plattform and record a preview**.
5. **Upload the preview image and video** in the Spark AR hub and **publish your effect**.

Now **Facebook will review your submission**. Officially this takes up to 10 working days, but in my experience it has always been less. Two working days are usually the maximum.

## Problems to look out for

If the **audio playback only works _after_ the recording of the video**, you have the microphone still enabled. An AR experience created with Spark AR can't simultaneously play an audio clip and record audio via the internal microphone. You can **disable the microphone** to enable audio playback during the recording process.

Should an **audio clip only play on Apple devices**, then your audio file is in the wrong codec: Spark AR supports ALAC as codec, but your audio won't be played on Android devices. **Convert your file to the AAC codec**.

If your **shader looks different in Spark AR than on your device**, the issue could be because of float precision. SparkSL only supports 16-bit floats, more about this [here](https://sparkar.facebook.com/ar-studio/learn/sparksl/cross-device-shader-sparksl#avoid). You should be careful when normalizing values or making use of exponential functions. SparkSL also provides [utility functions like "safeNormalize"](https://sparkar.facebook.com/ar-studio/learn/sparksl/sparksl-api/utils) to help you avoid such problems.


## Useful Ressources

### Offical Ressources

Official **assets for face filter** creation can be found here: [lookaside.facebook.com/developers/resources/?id=Face-reference-assets-classic.zip](https://lookaside.facebook.com/developers/resources/?id=Face-reference-assets-classic.zip)

_(Should the link to the assets be moved in the future, you might find the new one in [this page of the documentation](https://sparkar.facebook.com/ar-studio/learn/articles/people-tracking/face-reference-assets))_

The official **Blender Toolkit** for mesh optimazition, analysis and export can be found here: [lookaside.facebook.com/developers/resources/?id=Spark-AR-toolkit.zip](https://lookaside.facebook.com/developers/resources/?id=Spark-AR-toolkit.zip)

_(Should the link to the assets be moved in the future, you might find the new one in [this page of the documentation](https://sparkar.facebook.com/ar-studio/learn/articles/creating-and-prepping-assets/toolkit-for-blender))_


### Unofficial Ressources

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