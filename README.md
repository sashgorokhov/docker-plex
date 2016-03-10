# Supported tags and respective `Dockerfile` links

-	[`latest` (*Dockerfile*)](https://github.com/sashgorokhov/docker-plex/blob/master/Dockerfile)

[![](https://badge.imagelayers.io/sashgorokhov/plex:latest.svg)](https://imagelayers.io/?images=sashgorokhov/plex:latest 'Get your own badge on imagelayers.io')

# Plex

Plex is a media player system and software suite comprising many player applications for 10-foot user interfaces, and an associated media server that organizes personal media stored on local devices. It organizes audio (audiobooks, music, and podcasts) and visual (photos and videos) content from personal media libraries and streams it to mobile devices, smart TVs, and streaming boxes.

> [https://en.wikipedia.org/wiki/Plex_(software)](https://en.wikipedia.org/wiki/Plex_(software))

![logo](https://worldvectorlogo.com/logos/plex.svg)

# How to use this image

```console
$ docker run --name plex --net="host" -p 32400:32400 -v /media:/media -d sashgorokhov/plex
```
`--net="host"` parameter is needed to access plex server from outside the network.


This will start a Plex Media Server listening on the default port of 32400.
Then access it via `http://localhost:32400` or `http://host:32400` in a browser.

Image's supported volumes:
- `/media` - servers media root
- `/var/lib/plexmediaserver` - servers data directory

# Supported Docker versions

This image is officially supported on Docker version 1.10.2.
Support for older versions (down to 1.6) is provided on a best-effort basis.
Please see [the Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade your Docker daemon.
