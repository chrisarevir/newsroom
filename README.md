# April Fools 2021

Contains files and settings used to create the zoom illusion of a newsroom as we report the breaking news from this year.

In order to make it work with zoom, we are using OBS, a free, broadcasting/streaming software to trick zoom into thinking a composed video stream is a normal camera.

Using the following setup paired with the files found in this repo, you too can recreate this scenario!

## Setup

Create your scene in OBS with the + icon in the bottom left, name it whatever you'd like, and then start adding some sources.

For best results, add these in the following order to layer them correctly on your side of the stream.

<img width="372" alt="image" src="https://user-images.githubusercontent.com/1761533/113092577-1ac8dc00-91a3-11eb-9e61-c1a37d309cb1.png">

## Layers

The First two are text blocks and are the "dynamic" text that will appear to be a part of the top line on the overlay. Feel free to change the "Troy & Christian" layer to be your name or your segments name if you like, but do keep the DST News bit for consistency!

Ticker and Overlay read from "browser sources", but we are taking advantage of the fact that you can point it to local files. You can find the corresponding html pages to point those two layers towards named the same here.

Camera is slightly trickier. If you have an actual green screen, feel free to point it directly to your camera of choice. If you are like us, you can fake a very convincing green screen by routing your desired camera to [Snap Camera](https://snapcamera.snapchat.com), applying the greenscreen effect on it, and then in OBS choosing the SnapCamera as the source. This lets you have a background while having the foreground overlays still on top for proper layering. This is achieved by adding a filter on the camera in it's settings that is a "chroma key" filter. The automatic settings (green) should be good enough here, but if you run into trouble, feel free to ping us for troubleshooting.

The background layer is the video layer that needs to be set to loop upon completion. It has no sound, but, but is very convincing to have the background be a "live studio" loop.

## Getting it into Zoom

Cool, you have all of that setup, but now how in the world do you get it to pipe to zoom?
Thats actually easy to do! Just start the virtual camera (which sould be a button on the bottom left). AFter doing that, that "camera" should appear in zoom as a camera option, and VOILA! You no have a working newsroom environment to cast from from zoom!
