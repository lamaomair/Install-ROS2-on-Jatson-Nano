# Install-ROS2-on-Jetson-Nano
## This repository represent the steps to install (ROS2) into Jetson nano


### 1- Open a new terminal

### 2- Set up the Jetson Nano to accept software from packages.ros.org :

$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

### 3- Add a new apt key:

$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

### 4- Update the Debian packages index:

$ sudo apt update

### 5- Install the ROS Desktop package :

$ sudo apt install ros-melodic-desktop

### 6- load the ROS environment variables automatically when you execute a new shell session.

$ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
$ source ~/.bashrc

### 7- Install and initialize rosdep :

$ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
$ sudo rosdep init
$ rosdep update

## Now the Jetson Nano is ready to execute ROS packages.
https://docs.ros.org/en/dashing/Installation/Ubuntu-Install-Debians.html

