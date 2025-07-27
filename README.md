<p align="left">
    <!-- Discord Badge -->
    <a href="https://discord.justus0405.com/"><img src="https://img.shields.io/discord/1370519315400495234?logo=Discord&colorA=1e1e2e&colorB=a6e3a1&style=for-the-badge"></a>
    <!-- Version Badge -->
    <a href="https://github.com/Justus0405/ShellCam/blob/main/ShellCam.sh"><img src="https://img.shields.io/badge/Version-1.0-blue?colorA=1e1e2e&colorB=cdd6f4&style=for-the-badge"></a>
</p>

<p align="left">
    <!-- Stars Badge -->
	<a href="https://github.com/Justus0405/ShellCam/stargazers"><img src="https://img.shields.io/github/stars/Justus0405/ShellCam?colorA=1e1e2e&colorB=b7bdf8&style=for-the-badge"></a>
    <!-- Issues Badge -->
	<a href="https://github.com/Justus0405/ShellCam/issues"><img src="https://img.shields.io/github/issues/Justus0405/ShellCam?colorA=1e1e2e&colorB=f5a97f&style=for-the-badge"></a>
    <!-- Contributors Badge -->
	<a href="https://github.com/Justus0405/ShellCam/contributors"><img src="https://img.shields.io/github/contributors/Justus0405/ShellCam?colorA=1e1e2e&colorB=a6da95&style=for-the-badge"></a>
</p>

# ShellCam

ShellCam is a simple command-line tool for Linux that lets you create a virtual webcam. You can use it to show images, play local video files, or stream video from a URL directly to the virtual webcam. This can be useful for video calls, testing, or streaming. It uses `v4l2loopback` to create the virtual webcam and `ffmpeg` to handle the video input.

# Examples

This allows you, for example, to use your phone as a webcam. Just install the [IP Webcam App](https://play.google.com/store/apps/details?id=com.pas.webcam), start the video stream, and use the address shown at the bottom like this:

```shell
   shellcam-cli remote start http://192.168.178.75:8080/video
```

> [!NOTE]
> The `/video` part is important!
> You can configure rotation, resolution, front or back camera, etc., inside the app. I suggest starting at 720p, depending on your wireless speed.

If you want to set a locally stored image or video as your camera, you can do it like this:

```shell
   shellcam-cli viurtal start ~/Pictures/image.png
```

## Dependencies

```plaintext
   v4l2loopback-dkms
   ffmpeg
```

## Installation

1. Clone the repository:

   ```shell
   git clone https://github.com/Justus0405/ShellCam.git
   ```

2. Navigate to the directory:

   ```shell
   cd ShellCam
   ```

3. Make the script executable:

   ```shell
   chmod +x shellcam-cli
   ```

4. Run the script with the install argument:
   ```shell
   ./shellcam-cli install
   ```

## Usage

```plaintext
usage: shellcam-cli [...]
arguments:
         install
         uninstall
         udpate
         remote start URL
         remote stop
         virtual start FILEPATH
         virtual stop
         stop
         status
         help
         version
```

#

<p align="center">
	Copyright &copy; 2025-present <a href="https://github.com/Justus0405" target="_blank">Justus0405</a>
</p>

<p align="center">
	<a href="https://github.com/Justus0405/ShellCam/blob/main/LICENSE"><img src="https://img.shields.io/github/license/Justus0405/ShellCam?logo=Github&colorA=1e1e2e&colorB=cba6f7&style=for-the-badge"></a>
</p>
