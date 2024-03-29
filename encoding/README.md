# Encoding 

## :one: Install

:pushpin: Install [`MP4Box`](https://formulae.brew.sh/formula/gpac)

:bulb: Test if installed

```
% brew info gpac | grep nstalled 
Not installed
```

```
% brew install gpac
```

:pushpin: Install [`ffmpeg`](https://formulae.brew.sh/formula/ffmpeg)

```
% brew install ffmpeg
```



# :two: Roll

- [ ] go to `scripts` folder and generate the streaming files that will be located under `stream` folder

```
cd scripts; sh encode-all.sh
```


- [ ] Run the python server

```
python PythonServer.py
```


- [ ] Test using the below URL where IP is your host i.e. `localhost` or `192.168.1.100`

```
http://<IP>:8000
```

- [ ]  select any of these html files

|:hash:| Platform        | [Raw Dash](scripts/raw-dash.html) | [Raw Hls](scripts/raw-hls.html) | [MES Dash](scripts/mes-dash.html)| [MES Hls](scripts/mes-hls.html) |
|------|-----------------|-----------------------------------|---------------------------------|----------------------------------------|---------------------------------|
| 01   | Desktop/Chrome  | :x:                               | :x:                             | :heavy_check_mark: :sound: | :heavy_check_mark:  :movie_camera: |
| 02   | Desktop/Safari  | :x:                               | :heavy_check_mark: :sound:        | :heavy_check_mark: :sound: | :x: |
| 03   | Desktop/Firefox | :x:                               | :x:                             | :heavy_check_mark: :sound: | :heavy_check_mark:  :sound: |
| 04   | iOS/Safari      | :x:                               | :heavy_check_mark: :movie_camera: | :x: | :heavy_check_mark:  :movie_camera: |
| 05   | iOS/Firefox     | :x:                               | :heavy_check_mark: :movie_camera: | :x: | :heavy_check_mark:  :movie_camera: |
| 06   | Android/Chrome  | :x:                               | :x: | :heavy_check_mark: :sound: | :x:   |

# References:

MES: Media Source Extension

### :sound: <sup>audio only</sup>
### :movie_camera: <sup>audio/video</sup> 

https://caniuse.com/#feat=mediasource


## Documentation to read

- [ ] [Creating A Production Ready Multi Bitrate HLS VOD stream](https://docs.peer5.com/guides/production-ready-hls-vod)
- [ ] [Self-hosting videos with HLS](https://www.exoscale.com/syslog/self-hosted-videos)
- [ ] [How to read mp3 tags in shell?](https://askubuntu.com/questions/226773/how-to-read-mp3-tags-in-shell)
- [ ] [How Netflix protects its content — Part 1](https://medium.com/pallycon/how-netflix-protects-contents-part-1-a40508ed0001)
- [ ] [Converting an HLS (m3u8) to MP4](https://stackoverflow.com/questions/33108105/converting-an-hls-m3u8-to-mp4)

```
ffmpeg -i https://oo.com/ddd/ddd//video.m3u8 -acodec copy -bsf:a aac_adtstoasc -vcodec copy out.mp4
```


:round_pushpin: ffmpeg JS

- [ ] [Port of FFmpeg with Emscripten ](https://github.com/Kagami/ffmpeg.js)
- [ ] [FFmpeg for browser and node, powered by WebAssembly ](https://github.com/ffmpegwasm/ffmpeg.wasm)

:round_pushpin: HLS Book
- [ ] [How to Serve HLS Video from an S3 Bucket](https://hlsbook.net/how-to-serve-hls-video-from-an-s3-bucket)
- [ ] [How to Encrypt Video for HLS](https://hlsbook.net/how-to-encrypt-hls-video-with-ffmpeg)


