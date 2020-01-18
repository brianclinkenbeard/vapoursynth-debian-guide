## Install VapourSynth on Debian Bullseye
### Installing dependencies from respositories
```
sudo apt-get install \
autoconf \
automake \
pkg-config \
build-essential \
python3-dev \
python3-pip \
cython3 \
libmagick++-dev \
libarchive-dev
```
### Installing zimg
```
git clone https://github.com/sekrit-twc/zimg.git
cd zimg
./autogen.sh
./configure --enable-x86simd
make
sudo make install
```
Note that you can also use `sudo checkinstall` instead of `sudo make install` to have the ability to uninstall with dpkg.

### Installing VapourSynth
```
git clone https://github.com/vapoursynth/vapoursynth.git
cd vapoursynth
./autogen.sh
./configure
make
sudo make install
sudo ldconfig
```
Again, you may also use `checkinstall`.

### Install Python wrapper
```
pip3 install VapourSynth
```

### Install VapourSynth editor (optional)
```
sudo apt-get install qt5-default libqt5websockets-dev
git clone https://bitbucket.org/mystery_keeper/vapoursynth-editor.git
cd vapoursynth-editor/pro
qmake pro.pro
make
```
Binaries can now be found in `../build`.
