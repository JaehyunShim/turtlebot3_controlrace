# Turtlebot3 Control Race!!!!!!

## Usage

### Install ROS 2 Dashing
```sh
$ sudo apt update && sudo apt upgrade
$ wget https://raw.githubusercontent.com/rjshim/yolo_test/master/install_ros_kinetic.sh && chmod 755 ./install_ros_kinetic.sh && bash ./install_ros_kinetic.sh
```
### Install ROS packages and Build
```sh
(Move to your workspace)
$ cd ~/robotis_ws/src/

(Download packages)
$ git clone https://github.com/rjshim/yolo_test.git
$ git clone https://github.com/ROBOTIS-GIT/DynamixelSDK.git

(Install binary packages)
$ sudo apt-get install ros-kinetic-uvc-camera
$ sudo apt-get install ros-kinetic-sound-play
$ sudo apt-get install ros-kinetic-darknet-ros-msgs

(Build)
$ cd ~/catkin_ws && catkin_make
```

### Execute ROS packages
```sh
(uvc camera)
$ rosrun uvc_camera uvc_camera_node /image_raw:=/camera/image_raw

(robot controller)
$ rosrun robot_controller robot_controller
```

## TODO
- Set material for the custom Collada file (Can be done with Blender???).
- Implement friction on the horizontally moving obstacle.

## Reference
- [DynamixelSDK](https://github.com/ROBOTIS-GIT/DynamixelSDK)
