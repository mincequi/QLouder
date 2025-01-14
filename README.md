# qLouder
A tool to measure and design loudspeakers.

It is loosely inspired by the famous [Room EQ Wizard](https://www.roomeqwizard.com).
However, it aims to provide a better user experience as well as pleasing aesthetics.
qLouder can also be considered as the successor of qloud:  
http://gaydenko.com/qloud/  
https://github.com/molke-productions/qloud/

<img src="https://user-images.githubusercontent.com/1805183/160924496-d879493e-a46a-47d0-a49e-e64d4e891b1a.png" width="480">

<img src="https://user-images.githubusercontent.com/1805183/192761720-a34e9364-b5f3-4c61-bf78-8d4831ef311f.png" width="480">

# Target use
The measurement and design features of qLouder can help you to create an 
optimal filter set and crossover for your DIY loudspeaker.

# Measurement process
* generate and play back an audio test signal (sine sweep) via sound card, amplifier and loudspeaker box
* measure signal via measurement microphone
* generate impulse response from recorded signal
* time gate impulse response
* generate frequency response
* apply microphone calibration file
* design a target curve (house curve)
* design correction filters to match your target curve
* design a crossover for your 2-way speaker

# Current features
* Sine sweep generation (including proper windowing).
* Time gating of measured impulse response
* Microphone calibration
* Crossover
* Loudness based house curve
* Parametric equalizer
* Different sample rates for playback and recording
* Simple music player

# TODO
* Port to Qt6
* SPL meter
* Persistent measurements
* ~~Harman house curve~~
* Separate handlers for bass and treble for loudness target
* Remove QtMultimedia and use miniaudio instead
* Detect hot plugged audio devices
* Improve crossover handles for order of 4
* Improve equalizer handles for shelving filters
* Align crossover filter settings to equalizer filter settings

# Requirements
* GCC >= 9.4.0
* Qt >= 5.12 (Qt6 not yet supported)
* e.g. Ubuntu >= 20.04 (Focal)
* PulseAudio is running

# Installation (based on Ubuntu)
```
sudo apt install \
  zlib1g-dev \
  libcurl4-openssl-dev \
  libfftw3-dev \
  libfontconfig1-dev \
  libgl-dev \
  libmpg123-dev \
  libpulse-dev \
  libsndfile1-dev \
  libtag1-dev \
  libxcursor-dev \
  libxi-dev \
  libxinerama-dev \
  libxrandr-dev \
  pkgconf \
  qtbase5-dev \
  qtdeclarative5-dev \
  qtmultimedia5-dev \
  qtquickcontrols2-5-dev \
  qml-module-qtcharts \
  qml-module-qtquick-dialogs \
  qml-module-qtquick-shapes \
  qml-module-qt-labs-folderlistmodel \
  qml-module-qt-labs-settings \
  libqt5charts5-dev \
  libqt5svg5-dev \
  libqt5multimedia5-plugins

git clone https://github.com/mincequi/qLouder
cd qLouder
mkdir build && cd build
cmake ..
make
```

# Contribute
Contributations are always welcome. In the best case in the form of a pull request :)
