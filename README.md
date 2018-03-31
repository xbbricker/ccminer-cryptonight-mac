
Binaries for CUDA mining on macOS, built from [KlausT/ccminer-cryptonight](https://github.com/KlausT/ccminer-cryptonight).

## Setup

To mine with ccminer-cryptonight-mac, you'll need to download and install the following:

1. [An NVIDIA web driver compatible with your macOS build number](https://www.insanelymac.com/forum/forums/topic/324195-nvidia-web-driver-updates-for-macos-high-sierra-update-03302018)
	* Go to Apple > About This Mac, and click on the Version number to reveal the build number

2. [A CUDA driver, v387.128 or newer](https://www.nvidia.com/object/mac-driver-archive.html)
	* Must support CUDA API 9.1

3. [The ccminer executable and CUDA runtime library.](https://github.com/xbbricker/ccminer-cryptonight-mac/releases/download/3.01/ccm-301.zip)

## Usage

See
`./bin/ccminer -h`
or
[this README](https://github.com/KlausT/ccminer-cryptonight/blob/master/README.md)

## Build Guide

#### Install macOS command line tools
```
xcode-select --install
```
#### Install Homebrew (https://brew.sh)
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### Install CUDA Toolkit 9.1+
```
hdiutil attach https://developer.nvidia.com/compute/cuda/9.1/Prod/network_installers/cuda_9.1.128_mac_network
open -a /Volumes/CUDAMacOSXInstaller/CUDAMacOSXInstaller.app
```
#### Install build dependencies
```
brew install openssl autoconf automake
```
#### Build

```
git clone -b mac https://github.com/xbbricker/ccminer-cryptonight-mac
cd ccminer-cryptonight-mac
./autogen.sh
./configure
```


Changelog
-
* [March 31, 2018] Rebased on KlausT's repo
	* Compatabile with Monero's upcoming PoW tweak
* [Dec 12, 2017] Updated to support CUDA 9.0 (only)
	* Dropped support for compute version 2.0