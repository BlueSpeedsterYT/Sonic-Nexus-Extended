# Sonic Nexus Extended
[WARNING: Unless you do plan on supporting the project, please do not download the source code and attempt to build it, as content from development could potentially result into failure and an unstable build of Nexus Extended ready. Be sure to always download the latest stable version as its available from the Releases tab.]

This is a modified version of the Sonic Nexus (2008) Decompiliation.
This will require the player to have a copy of the assets from the originial Sonic Nexus release, download is available [here](https://info.sonicretro.org/Sonic_Nexus).

# New Features
* Allowing support for multiple playable characters (In Development)
* A new max Value limit of 20. (Not that anyone would use that anyways lmao)
* A new set of variables to allow the game to run without any issues in either 4:3 or 16:9 (Available, but it is being tested.)

# Returning Tweaks from the Decomp
* Added a built in mod loader, allowing to easily create and play mods.
* There is now a `settings.ini` file that the game uses to load all settings, similar to Sonic Mania (Plus).
* Dev menu can now be accessed from anywhere by pressing the `ESC` key if enabled in the config.
* The `F12` pause, `F11` step over & fast forward debug features from Sonic Mania (Plus) have all been ported and are enabled if `devMenu` is enabled in the config.

# How to build
## Windows
* Clone the repo, then follow the instructions in the [depencencies readme for Windows](./dependencies/windows/dependencies.txt) to setup dependencies, then build via the visual studio solution.
* Alternatively, you can grab a prebuilt executable from the releases section.

## Mac
* Clone the repo, follow the instructions in the [depencencies readme for Mac](./dependencies/mac/dependencies.txt) to setup dependencies, then build via the Xcode project.

## Linux
* To setup your build enviroment and library dependecies, run the following commands:
  * Ubuntu (Mint, Pop!_OS, etc...): `sudo apt install build-essential git libsdl2-dev libvorbis-dev libogg-dev libtheora-dev`
  * Arch Linux: `sudo pacman -S base-devel git sdl2 libvorbis libogg libtheora`
* Clone the repo with the following command: `git clone https://github.com/Rubberduckycooly/Sonic-Nexus-Decompilation.git`
* Go into the repo you just cloned with `cd Sonic-Nexus-Decompilation`.
* Then run `make CXXFLAGS=-O2 -j5`.
  * If your distro is using gcc 8.x.x, then add the argument `LIBS=-lstdc++fs`.
  * The `CXXFLAGS` option can be removed if you do not want optimizations.
  * -j switch is optional, but will make building faster by running it parallel on multiple cores (8 cores would be -j9.)

## Other Platforms
Currently the only supported platforms are the ones listed above, however the backend uses libogg, libvorbis, libtheora & SDL2 to power it, so the codebase is very multiplatform. If you're able to, you can clone this repo and port it to a platform not on the list.

# Contact:
Join the [Retro Engine Modding Discord Server](https://dc.railgun.works/retroengine) for any extra questions you may need to know about the decompilation or modding it.
