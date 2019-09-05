# Turtlebot3 Control Race (a.k.a. gazebo playground!!!!!)

## Usage
- Control TB3 on Gazebo with Teleop Keyboard and Run to the Goal Point in 2 min. 

### Install ROS 2 Dashing
```sh
$ sudo apt update && sudo apt upgrade
$ wget https://raw.githubusercontent.com/rjshim/turtlebot3_controlrace/master/install_ros_dashing.sh?token=AJGY62JYSEDMLJB6L5LEIQ25OB5AS && chmod 755 ./install_ros_dashing.sh && bash ./install_ros_dashing.sh
```
### Install ROS packages and Build
```sh
(Move to colcon workspace)
$ cd ~/robotis_ws/src/

(Download packages)
$ git clone https://github.com/rjshim/turtlebot3_controlrace.git

(Install relevant packages)
http://emanual.robotis.com/docs/en/platform/turtlebot3/ros2/#pc-setup

(Build)
$ cd ~/robotis_ws && colcon build --symlink-install
```

### Execute ROS packages
```sh
(Set Gazebo Model and Plugin paths)
$ export GAZEBO_MODEL_PATH=$HOME/robotis_ws/src/turtlebot3_controlrace/models
$ export GAZEBO_PLUGIN_PATH=$HOME/robotis_ws/src/turtlebot3_controlrace/models/turtlebot3_controlrace/turtlebot3_controlrace_plugin/build

(Gazebo with a virtual TB3)
$ ros2 launch turtlebot3_controlrace turtlebot3_controlrace.launch.py

(teleop keyboard)
$ ros2 run turtlebot3_teleop teleop_keyboard
```

## TODO
- Set material for the custom Collada file (Can be done with Blender???).
- Implement friction on the horizontally moving obstacle.
- Display current time.
- Implement the goal line + plugin.

## Reference
- [DynamixelSDK](https://github.com/ROBOTIS-GIT/DynamixelSDK)
