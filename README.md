# Ros_RobotArm

## How to download VirtualBox and Ubuntu 18.04
To begin with, it is necessary to obtain the VirtualBox software and the Ubuntu 18.04.6 operating system in order to proceed with the installation of both the ROS (Robot Operating System) and the robot arm.

## How to install Ros melodic
After obtaining the required software, you can open a terminal and execute the following commands to install ROS Melodic on your computer:
```
$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
$ sudo apt update
$ sudo apt install ros-melodic-desktop-full
$ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
$ source ~/.bashrc
$ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
$ sudo apt install python-rosdep
$ sudo rosdep init
$ rosdep update
```
## To install the Catkin workspace, you can follow these steps:
```
$ sudo apt-get install ros-melodic-catkin
$ source /opt/ros/melodic/setup.bash
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
$ cd ~/catkin_ws/src
```
## To install the robot arm, you can follow these steps
```
$ sudo apt install git
$ git clone https://github.com/smart-methods/arduino_robot_arm.git 
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src -r -y
$ sudo apt-get install ros-melodic-moveit
$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
$ catkin_make
$ sudo nano ~/.bashrc
$ source ~/.bashrc
$ roslaunch robot_arm_pkg check_motors.launch
```

## Robot arm on rviz
After completing the installation and setup process, you should be able to launch the robot arm in RViz. The RViz visualization tool allows you to interact with the robot arm and simulate its movements.

![image](https://github.com/Zahrah794/Ros_RobotArm/assets/139267881/ee8c1307-b81b-47ad-a3d1-cd2bc78ab538)








