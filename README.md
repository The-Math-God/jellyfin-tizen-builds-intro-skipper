# jellyfin-tizen-builds-with-intro-skipper-support

this has been modified to have intro-skipper plugin support

due to 10.8.12 being the latest custom webui for intro skipper 
until newer versions are made i can't make any updates

credit to (https://github.com/Bobby306/intro-skipper) for the custom webui files which made this possible 

## Installation
For a one step install process using Docker, check out this guide made by Georift [Georift/install-jellyfin-tizen](https://github.com/Georift/install-jellyfin-tizen).

### Prerequisites
- Tizen Studio with CLI (https://developer.tizen.org/development/tizen-studio/download)
- One of the .wgt files from a release (https://github.com/The-Math-God/jellyfin-tizen-builds-with-intro-skipper-support/releases)

### Getting Started
1. Install prerequisites. Yup nothing else needed.

### Deploy to TV
1. Activate Developer Mode on TV (https://developer.samsung.com/tv/develop/getting-started/using-sdk/tv-device).
2. Connect to TV with Device Manager from Tizen Studio. Typically located in `C:\tizen-studio\tools\device-manager\bin`
3. Install the package.  
   This command assumes the file you are installing is called `Jellyfin.wgt`. Simply change it to `Jellyfin-prerelease.wgt` if you are installing the prerelease version. Otherwise you can also just rename the file.
```bash
c:\tizen-studio\tools\ide\bin\tizen.bat install -n jellyfin.wgt -t <the name of your tv>
```
typically located in (C:\tizen-studio\tools\ide\bin)
> You can find your tv name in Device Manager from Tizen Studio or using `sdb devices`.  

## Common issues

### Install failing due to wrong certificate?

This should only happen if you already have a version installed using a different build certificate.  
This can be solved by uninstalling the app prior to attempting to install this version.

Removing it from the app bar is also not the same as removing it from the device, you need to actually go into the applications menu and remove it from there.
