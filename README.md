# AVShack (Alpha)

AVSHack is a Linux live streaming server that supports Ingesting, Mixing with Mix Minus, MultiMux, Multistreaming and Recording of RTMP, RTSP, SRT, and MP4 with LL-HLS and WebTransport Viewing.

The ingested sources can be mixed together into a single stream. The mix can be multistreamed to custom RTMP and SRT destinations;
pulled via multimux with rtmp, rtsp or srt; or viewed via LL-HLS or WebTransport.

Configuration is done via a web frontend or a REST api.  The web frontend utilizes the REST api.

Currently, the datastore is SQLite.

# Screenshot

![AVShack Screenshot](https://sparksandmagic.nyc3.digitaloceanspaces.com/sintelPipBigBuckBunny.png)

# Getting Started

## Create an Admin User

```bash
./avshack --add-admin-email='name@host.com'
```

## Start AVShack on Port 8080

```bash
./avshack
```

A directory call "AVShack" will be created.  Logs and the SQLite database will be stored there.

Finally, access in the browser at http://ip.address:8080/admin

## Formats

- RTMP
- RTSP
- SRT
- MP4
- H264
- H265
- AAC

## Operating Systems

Presently, Linux x64 has been tested, although, arm64 may work.

## Requirements

Mixing requires Nvidia CUDA and FFmpeg 7.1.1. Tested on a NVIDIA GeForce GTX 1650.

WebTransport Viewer requires Http/3 via QUIC and SSL.

## Wiki

Please see the wiki for more.

[Wiki](https://github.com/Sparks-And-Magic/AVShack/wiki/Home)

## Limitations

WebTransport player has only been tested on Desktop Chrome and Firefox.

## Subscription

This is subscription software that includes a time-limited free mode.

The time limit starts after streaming starts and is two hours of streaming.

## Free Trial

There is a 45 day free trial.

## Caveats

There is some CPU usage at idle.

## Contact

Feel free and reach out brian ~~~ sparksandmagic.com (replace ~~~ with @), especially if you need a feature we don't currently support.

##
