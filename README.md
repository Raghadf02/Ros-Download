This ReadMe file goes through the steps to download Ros Noetic to Ubuntu 20.04 and provide a simplified explanation of each step

**First step is setting up sources to accept software from packages.ros.org.**
This enable easy software managment and updates
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
**Setting up keys.**
The keys are a cryptography algorithm used to verify authenticity and protect the system 
```
sudo apt install curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
**Updating debian package and upgrading it.**
A Debian package is a format for bundling and distributing software on Debian-based systems like Ubuntu. Updating it ensure security, fix bugs and add features.
```
sudo apt update
sudo apt upgrade
```
**Downloading ros desktop full install.**
There are multiple ways to install ros packages. desktop full install downloads everything in desktop plus 2D/3D simulators and perception packages.
```
sudo apt install ros-noetic-desktop-full
```
**Installing dependencies.**
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```
**Initializing ros.**
rosdep enables easy instillation of system dependencies when compiling a sourcse
```
sudo apt install python3-rosdep
sudo rosdep init
rosdep update
```
