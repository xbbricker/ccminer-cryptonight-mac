# ccminer-cryptonight-mac
Binaries for CUDA mining on macOS, built from [tsiv/ccminer-cryptonight.](https://github.com/tsiv/ccminer-cryptonight)

Setup
--
To run this program, you'll need to have installed:

* [NVIDIA CUDA 8.0 driver](https://www.nvidia.com/object/macosx-cuda-8.0.90-driver.html)

* The "web" driver appropriate for your macOS version
  * [El Capitan: 10.11.6](http://www.nvidia.com/download/driverResults.aspx/114670/en-us).
  * [Sierra: 10.12.6](http://www.nvidia.com/download/driverResults.aspx/120845/en-us)
  * [Search Other Versions (Untested)](https://www.google.ca/search?q=site:www.nvidia.com/download/driverResults.aspx+10.x.x)

* The ccminer executable and CUDA runtime library. [download .zip](https://github.com/xbbricker/ccminer-cryptonight-mac/archive/CUDA-8-driver.zip)

Usage
-
See
`./bin/ccminer -h`
