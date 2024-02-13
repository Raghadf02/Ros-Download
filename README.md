Setting up sources to accept software from packages.ros.org
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
Setting up keys 
```
sudo apt install curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
Updating debian package and upgrading it
```
sudo apt update
sudo apt upgrade
```
downloading ros desktop full install
```
sudo apt install ros-noetic-desktop-full
```
installing dependencies 
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```
initializing ros
```
sudo apt install python3-rosdep
sudo rosdep init
rosdep update
```
