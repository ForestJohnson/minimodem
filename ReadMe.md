## minimodem - general-purpose software audio FSK modem
Copyright (C) 2011-2016 Kamal Mostafa <kamal@whence.com>

#### how to build this package for yourself on Linux (Debian/Ubuntu)

```
sudo apt install libsndfile1-dev fftw3-dev libasound2-dev libpulse-dev
sudo apt install pkg-config automake
 
aclocal
autoconf
autoheader
automake --add-missing

./configure
make
sudo make install

echo 'asdasdasdasd' | minimodem --tx 100

# If it sounds really scratchy, like its clipping or something, try re-doing the build
# but this time do

./configure --without-pulseaudio
make
sudo make install

```

Minimodem is a command-line program which decodes (or generates) audio
modem tones at any specified baud rate, using various framing protocols.
It acts a general-purpose software FSK modem, and includes support for
various standard FSK protocols such as Bell103, Bell202, RTTY, TTY/TDD,
NOAA SAME, and Caller-ID.

Minimodem can play and capture audio modem tones in real-time via the
system audio device, or in batched mode via audio files.

Minimodem can be used to transfer data between nearby computers using an
audio cable (or just via sound waves), or between remote computers using
radio, telephone, or another audio communications medium.

