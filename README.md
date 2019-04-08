This is a common utility that can help you to run any ffmpeg commands.It contains a RTSP helper that can recorder a video from RTSP stream.

## Nuget
https://www.nuget.org/packages/ColinChang.FFmpegHelper/
```sh
# .NET CLI
dotnet add package ColinChang.FFmpegHelper

# Package Manager
Install-Package ColinChang.FFmpegHelper
```
It's based on .net standard 2.0

## FFmpegHelper
FFmpegHelper can run a common ffmpeg command with the formate.`ffmpeg [beforeinput options] -i input [beforeoutput options] output`.We provide 2 screenshot methods inside it as a sample,you can extend any other useful common methods like what we provide.

## RtspHelper
RtspHelper is a useful utility based on FFmpegHelper to work with RTSP stream.It provides 3 functions.
* Recording.recording a specify RTSP stream to a video file
* Watermark.marking a picture watermark during recording.
* Screenshot.screenshot once or set a timer.

## Platforms
* Windows(x86,x64)
* macOS(x64)

This package is based on FFmpeg v4.4.1.Resources under [ffmpeg_v4.1.1](ffmpeg_v4.1.1) are from [FFmpeg officical Website](http://ffmpeg.org/download.html).You can download a newer version and replace it in the project.We are using the official shared version of ffmpeg package.

Since Linux has so many different version branches,we don't support it yet.FFmpeg provides built packages for Debian/Ubuntu/Fedora and Redhat only.For other versions and custom requirements,you can build FFmpeg from its source code.So here we don't provide linux support.
but we will handle it soon.

If you wanna extend Linux support,just edit [this place](https://github.com/colin-chang/FFmpegHelper/blob/master/ColinChang.FFmpegHelper/FFmpegHelper.cs#L96)

## Principle
We just packaged a library to transfer command to FFmpeg CLI.It's useful and simiple,except this,you also can use the FFmpeg API to use it for development.FFmpeg SDK only provide for baisc language like C.

## Guid
Check the sample project to see how to use it easily.
