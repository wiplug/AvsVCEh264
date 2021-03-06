
#AvsVCEh264
Avisynth to H.264 Video Encoding using OpenVideo Encode library that provides an OpenCL API that leverages the video compression engine (VCE) on AMD platforms.

## Usage

```
AvsVCEh264 -i input.avs -o output.264 -c myConfig.ini
```

##Configuration file
You can use configuration files located in configs folder or create your own.
If you have questions about settings values you can read and take as an example default_explained.ini configuration file.

## Requirements & Limitations
### Software
- The OpenVideo library is currently supported only on Windows 7 (maybe Vista).
- Lastest version of AviSynth. Download from [http://avisynth.nl/](http://avisynth.nl/ "official website").
- Catalyst driver release 12.8+.

### Hardware
- TrinityAPU, Radeon HD 7000 Series (Tahiti XT, CapeVerde) or newer GPU.
- At least 1.5 GB of free ram.

##Build
To build you need AMD APP SDK 2.7 or later and a compiler (Mingw, Microsoft Visual Studio 2008 or 2010)

##AMD:
VCE, OVC, OVE: It is unclear, in PDF documents referred to VCE (Video Codec Engine),
in the libraries (OpenVideo), the prefix used is OVE_ but I can not find anything on the internet about it.
AMD does not provide any documentation about its technology VCE, OVC or OVE.

## TODO
- Stdout output support.
- Set default input switch values for Output.
- Pause / ~~Cancel~~ buttons.
- Reduce number of global variables.
- Unicode support
- 64bit version
- Publish binaries
- Do case insensitive config file.

##Boring legal stuff

Copyright (c) 2013, David Gonzalez Garcia

AvsVCEh264 is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

AvsVCEh264 is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details. <http://www.gnu.org/licenses/>.


## History
- Fixed green bottom bar on videos whose height was not a multiple of 16.
- Now the encoding and decoding is done in separate threads and they make use of a circular buffer.
- Removed huge memory leak that held UV planes of all frames
- Added abort key (F8)
- Improved info shown during the encoding.
- Added monitor/info thread and buffer class
- Added sample config files (speed, quality & balanced)
- Added Timer class.
- New config system, now use .ini files.
- First release / prototype.

