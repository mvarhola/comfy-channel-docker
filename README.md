# comfy-docker

[**Docker**](https://www.docker.com/) image using custom-built [**FFmpeg**](http://nginx.org/en/) for deploying an instance of [**Comfy Channel**](https://github.com/mvarhola/comfy-channel) to stream to any RTMP stream intake service such as [**Twitch**](https://www.twitch.tv/).

## Supported tags and `Dockerfile` links

* [`latest` _(Dockerfile)_](https://github.com/mvarhola/comfy-channel-docker/blob/master/Dockerfile)

## Description

This [**Docker**](https://www.docker.com/) image can be used to create an instance of [**Comfy Channel**](https://github.com/mvarhola/comfy-channel). It is based on [**jrottenberg/ffmpeg**](https://github.com/jrottenberg/ffmpeg), and installs [**Python**](https://www.python.org/) and gets the latest version of [**Comfy Channel**](https://github.com/mvarhola/comfy-channel).

The main purpose is to allow streaming from [**Comfy Channel**](https://github.com/mvarhola/comfy-channel/) to a self-hosted server.

**GitHub repo**: <https://github.com/mvarhola/comfy-channel-docker>

**Docker Hub image**: <https://hub.docker.com/r/mvarhola/comfy-channel/>

## How to use

The fastest way to get set up is to run a container with this image. Specify your stream intake URL as **`SERVER_IP`** and **`STREAM_LOCATION`**

```bash
docker run --name comfy-channel -e "SERVER_IP=localhost" -e "STREAM_LOCATION=/live/stream" mvarhola/comfy-channel
```

To start an Nginx webserver for serving the stream, along with Comfy Channel, run the following docker-compose command

```bash
docker-compose up
```
