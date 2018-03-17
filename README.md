# Pepper Mapping

## Overview

Mapping with Softbank's Pepper platform using fake laserscan and [gmapping].

This work was created during a semester for the course 'Point of Sales Robotics' at the Aachen University of Applied Sciences.

### License

The source code is released under a [GNU General Public License, Version 3](LICENSE).

**Author(s): Mirko Reimbold**

The pepper_mapping package has been tested under [ROS] Kinetic Kame and Ubuntu 16.04.

## Installation

	cd ~/catkin_ws/src
	git clone https://github.com/mreimbold/pepper_mapping.git
	source ../devel/setup.bash
	rosdep install pepper_mapping

## Usage

Run the main node with

	roslaunch pepper_mapping pepper_mapping.launch

Run RViz to see the laser scan and the created 2D Map with

	roslaunch pepper_mapping pepper_mapping_rviz.launch

#### Dependencies
- [Robot Operating System (ROS)](http://wiki.ros.org) (middleware for robotics),
- [depth_image_proc](http://wiki.ros.org/depth_image_proc) (ROS Package to process depth images),
- [pointcloud_to_laserscan](http://wiki.ros.org/pointcloud_to_laserscan) (ROS Package to convert 3D Point Cloud to 2D laser scans),
- [gmapping](http://wiki.ros.org/gmapping) (ROS Package to provide laser-based SLAM (Simultaneous Localization and Mapping))

[ROS]: http://www.ros.org
[gmapping]: http://wiki.ros.org/gmapping

