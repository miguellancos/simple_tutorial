# Workstation Setup Tutorial

​	This tutorial is intended to help a correct setup of a workstation with CARLA Simulator and it's ROS Bridge integration. It was built based on logging all the steps taken in the configuration of another workstation, as such, it might be implementation dependent and you might have to face different problems than us.

## Initial conditions

​	The workstation used had the following specifications:

``` 
Processor: Intel(R) Core(TM) i3-4160 CPU @ 3.60GHz
RAM: 8Gb DDR3 1600MHz
Video Card: Nvidia GeForce GTX 770
Operative System: Xubuntu 18.04 64-bit (Bionic Beaver)
```

​	It is important to note that is was started with a clean installation of Xubuntu and all installed packages will be reported here.

## General dependencies

```bash
sudo apt-get update
sudo apt-get install wget software-properties-common
sudo add-apt-repository ppa:ubuntu-toolchain-r/test
wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key|sudo apt-key add -
sudo apt-add-repository "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-7 main"
sudo apt-get update
sudo apt-get install build-essential clang-7 lld-7 g++-7 cmake ninja-build libvulkan1 python python-pip python-dev python3-dev python3-pip libpng-dev libtiff5-dev libjpeg-dev tzdata sed curl unzip autoconf libtool rsync
pip2 install --user setuptools
pip3 install --user setuptools
sudo update-alternatives --install /usr/bin/clang++ clang++ /usr/lib/llvm-7/bin/clang++ 170
sudo update-alternatives --install /usr/bin/clang clang /usr/lib/llvm-7/bin/clang 170
```

## Installing Video Card drivers

In order to use the vulkan drivers you need to install the latest nvidia drivers. At the time of this writing 435 is the most recent.

```
sudo apt install nvidia-driver-435
```

