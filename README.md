# Motivation

This is a very simple h264 video player (that can run on live stream) for your browser.
You might use this with raspicam raw h264 stream.
This is a player around [Broadway](https://github.com/mbebenita/Broadway) Decoder, with very simple API.
NAL unit (h264 frames) are split on the server side, so the client side is very simple (and allow frame skipping easily)


# History
* I was targetting a real-time  camera video feedback (no audio/surveillance cam) in the browser
* There is no solution for "real time"  mp4 video creation / playback (ffmpeg, mp4box.js, mp4parser - _boxing_ _takes_ _time_)
* Media Source Extension is a dead end (mp4 boxing is far too hard to re-create on the client side)
* [Broadway](https://github.com/mbebenita/Broadway) provide the crazy emscripten/asm build of a h264 encoder accelerated by webGL canvas
* Here is all the glue we need, enjoy ;-)


# Installation/demo
```
npm install
grunt pack

# edit server.js to your needs, check server-tcp.js for relaying a rpi video
node .
# browse to http://127.0.0.1:8080/ for a demo player

```

# Recommandation
* Broadway h264 Decoder can only work with baseline profile
* Browserify FTW


# Credits
* [131](mailto:131.js@cloudyks.org)
* [Broadway](https://github.com/mbebenita/Broadway)
* [urbenlegend/WebStreamer](https://github.com/urbenlegend/WebStreamer)


# Keywords / shout box
raspberry, mp4box, h264, nal, raspivid, mse, media source extension, iso, raspicam, bitrate, realtime, video, mp4, ffmpeg, "Let's have a beer and talk in Paris"



