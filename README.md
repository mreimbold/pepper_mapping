# Pepper Mapping

[![ROS Kinetic Kame][ros-badge-image]][ros-badge-url]
[![Ubuntu 16.04][ubuntu-badge-image]][ubuntu-badge-url]

## Overview

Mapping with Softbank's Pepper platform using fake laserscan and [gmapping].

This work was created during a semester for the course 'Point of Sales Robotics' at the Aachen University of Applied Sciences.

### License

The source code is released under a [GNU General Public License, Version 3](LICENSE).

**Author(s): Mirko Reimbold**

## Prerequisites

This package has been tested under [ROS] Kinetic Kame and Ubuntu 16.04.

In order to use this package please follow [this tutorial](http://wiki.ros.org/pepper/Tutorials) to setup your Pepper platform properly.

As we use Pepper's depth camera you have to calibrate it, to do so you can follow [this tutorial](http://wiki.ros.org/pepper/Tutorials/Calibration#Depth_camera_calibration).

## Installation

	cd ~/catkin_ws/src
	git clone https://github.com/mreimbold/pepper_mapping.git
	source ../devel/setup.bash
	rosdep install pepper_mapping

## Usage

Starting the bridge on Pepper

	roslaunch pepper_bringup pepper_full.launch nao_ip:=<yourRobotIP> roscore_ip:=<roscore_ip> [network_interface:=<eth0|wlan0|vpn0>]

Run the main node with

	roslaunch pepper_mapping pepper_mapping.launch

Run RViz to see the laser scan and the created 2D Map with

	roslaunch pepper_mapping pepper_mapping_rviz.launch

#### Dependencies
- [Robot Operating System (ROS)](http://wiki.ros.org) (middleware for robotics),
- [naoqi_driver](https://github.com/ros-naoqi/naoqi_driver) (c++ bridge based on libqi)
- [depth_image_proc](http://wiki.ros.org/depth_image_proc) (ROS Package to process depth images),
- [pointcloud_to_laserscan](http://wiki.ros.org/pointcloud_to_laserscan) (ROS Package to convert 3D Point Cloud to 2D laser scans),
- [gmapping](http://wiki.ros.org/gmapping) (ROS Package to provide laser-based SLAM (Simultaneous Localization and Mapping))

[ROS]: http://www.ros.org
[gmapping]: http://wiki.ros.org/gmapping

[ros-badge-image]: https://img.shields.io/badge/ROS-Kinetic%20Kame-blue.svg
[ros-badge-url]: http://wiki.ros.org/kinetic/Installation
[ubuntu-badge-image]: https://img.shields.io/badge/Ubuntu-16.04-orange.svg
[ubuntu-badge-url]: https://www.ubuntu.com/

