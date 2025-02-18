# Picta Kodi Video Plugin

Video plugin for [Kodi](https://github.com/xbmc/xbmc) mediacenter. This Kodi Add-on provides a minimal interface for [Picta](https://www.picta.cu/).

## Features
- Discover new videos
- Play videos

## Requirements
- Python [requests](https://github.com/psf/requests) library packed for KODI
- Add-ons VideoPlayer InputStream
  - [Adaptive](https://github.com/xbmc/inputstream.adaptive)
  - [FFmpeg Direct](https://github.com/xbmc/inputstream.ffmpegdirect)
    - [Nexus](https://github.com/xbmc/inputstream.ffmpegdirect/tree/Nexus#build-instructions)
    - [Matrix](https://github.com/xbmc/inputstream.ffmpegdirect/tree/Matrix#build-instructions)

## Installation Kodi and InputStreams
For Kodi v19.4 (Matrix) and latest  releases

### Windows 10 / 11
```pwsh
winget install -e --id XBMCFoundation.Kodi
```

### Ubuntu 20.04.5 LTS (Focal Fossa) 
```bash
sudo apt install software-properties-common
sudo add-apt-repository -y ppa:team-xbmc/ppa
sudo apt install kodi
sudo apt install kodi-inputstream-adaptive kodi-inputstream-ffmpegdirect
```
### Archlinux AUR
[Package](https://aur.archlinux.org/packages/kodi-plugin-video-picta-bin) available for archlinux users

with yay
```bash
yay -S kodi-plugin-video-picta-bin
```

with paru
```bash
paru -S kodi-plugin-video-picta-bin
```

## Installation from Official Kodi Add-on repository
- Open Kodi, go to `Add-ons / Kodi Add-on repository / Video add-ons / Picta` and select `Install`

## Installation manual

* [Download the latest release](https://github.com/oleksis/plugin.video.picta/releases/latest) (`plugin.video.picta-kodi_19.zip`)
- Copy the zip file to your Kodi system
  - Windows: `%APPDATA%\Kodi`
  - Linux: `~/.kodi`
- Open Kodi, go to `Add-ons / Add-on browser` and select `Install from zip file`
- Select the file `plugin.video.picta-kodi_19.zip`

## Development
This plugin follow the code style from ["Very simple video plugin for Kodi mediacenter"](https://github.com/romanvm/plugin.video.example)

### Rules for plugins by [romanvm](https://github.com/romanvm)
- If a ListItem opens a lower lever list, it must have `isFolder = True`
- If a ListItem calls a playback function that ends with `setResolvedUrl`, it must have `setProperty('isPlayable', 'true')` and `isFolder = False`
- If a ListItem does any other task except for mentioned above, is must have `isFolder = False` (and only this)

## Other links
- [Add-on development](https://kodi.wiki/view/Add-on_development)
- [Create add-on PRs using Git Subtree Merging](https://kodi.wiki/view/HOW-TO:Create_add-on_PRs_using_Git_Subtree_Merging)
- [Create a Kodi add-on repository from add-on sources](https://github.com/chadparry/kodi-repository.chad.parry.org/blob/master/tools/create_repository.py)
- [HOW-TO:Install Kodi for Linux](https://kodi.wiki/view/HOW-TO:Install_Kodi_for_Linux)
- [Add-on:Inputstream FFmpeg Direct](https://kodi.wiki/view/Add-on:Inputstream_FFmpeg_Direct)

## Copyright and license

This add-on is licensed under the MIT License - see [LICENSE.txt](LICENSE.txt) for details.
