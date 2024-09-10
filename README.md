# AVShack (Beta)

VOD On-Premise Server App - Supports MP4, H264, H264, AAC, and HLS M3U8 Generation

Media server that can ingest MP4 files on disk and create HLS M3U8 links.  Also, has an embedded HLS.js player.

Configuration is done via a web frontend or a REST api.  The web frontend utilizes the REST api.

Currently, the datastore is SQLite.

# Getting Started

## Create an Admin User

```bash
$ ./avshack --add-admin-email='name@host.com'
```

## Start AVShack on Port 8080

```bash
$ ./avshack --urls='http://*:8080'
```

A directory call "AVShack" will be created.  Logs and the SQLite database will be stored there.

# Features

## VOD Directories

A directory, on disk, can be mapped to a url.  The files in the directory can be accessed via /hls/mapped_name/file.mp4
and /v/mapped_name/file.mp4.

So, if AVShack is running on localhost, then http://localhost/hls/mapped_name/file.mp4 will generate a HLS .M3U8 and 
http://localhost/v/mapped_name/file.mp4 serve a HLS.js player.

Multiple VOD directories can be defined.

## Playlists

A playlist, with file extension .pls, can be utilized.  It's a text file with one MP4 per line.  These MP4 files will be 
sent to the user, one after another.  Each MP4 must have the same settings.

The same settings are:

- Codec
- Profile and Level
- Audio: Sample Rate and Channels
- Video: Width and Height

## Formats

- MP4
- H264
- H265
- AAC

## Operating Systems

Presently, Linux x64 has been tested, although, arm64 is available.

If Windows is needed, please reach out (email below).

## Caveats

The Linux version uses some CPU usage at idle.

## Contact

Feel free and reach out brian ~~~ sparksandmagic.com (replace ~~~ with @), especially if you need a feature we don't currently support.
##
