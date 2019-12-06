## CARLA Simulator

​	While the Unreal Engine is compiling and installing, which might take a while, we can start by download the CARLA from the github. And then changing to the git folder.

```bash
git clone https://github.com/carla-simulator/carla
cd carla
```

​	We are using the latest development version of CARLA which is in the master branch. In case you want the latest stable version you need to change to the stable branch.

```bash
git checkout stable
```

​	Before we download the assets package we can install the `aria2` utility which will allow for a faster download, since it is quite big.

```bash
sudo apt install aria2
```

​	Now we can download the assets package by running the following script.

```bash
./Update.sh
```

