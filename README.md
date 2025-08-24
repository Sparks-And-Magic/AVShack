# AVShack (Beta)

Live Stream Mixing On-Premise Server App. Supports RTMP, RTSP, SRT, and MP4 ingest. The ingested
sources can be mixed together into a single stream. The mix can be multistreamed custom RTMP and SRT destinations.

Also, viewing via Ultra-Low Latency WebTransport and LL-HLS is supported.

Configuration is done via a web frontend or a REST api.  The web frontend utilizes the REST api.

Currently, the datastore is SQLite.

# Getting Started

## Create an Admin User

```bash
$ ./avshack --add-admin-email='name@host.com'
```

## Start AVShack on Port 8080

```bash
$ ./avshack
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

Presently, Linux x64 has been tested, although, arm64 is available.

## Requirements

FFmpeg 7.1

Mixing requires a GPU. Tested on a NVIDIA GeForce GTX 1650.

## Limitations

The free version is limited to two hours of live streaming.

WebTransport player has only been tested on Desktop Chrome and Firefox.

## Free Trial

There is a 45 day free trial.

## Caveats

The Linux version uses some CPU usage at idle.

## Contact

Feel free and reach out brian ~~~ sparksandmagic.com (replace ~~~ with @), especially if you need a feature we don't currently support.

##
