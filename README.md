# Livox Laser Simulation

A package to provide plug-in for [Livox Series LiDAR](https://www.livoxtech.com).

This package is currently in development to support Ubuntu 20.04, ROS Noetic Ninjemys, and Gazebo 11 and will be tailored for the needs of Silolytics. It is not recommened to use this package in its current state.

## Requirements

- Ubuntu [20.04](https://releases.ubuntu.com/20.04/)
- ROS [Noetic Ninjemys](http://wiki.ros.org/noetic/)
- Gazebo [11](http://gazebosim.org/)

## Results

- avia

![](resources/avia.gif)

- mid40

![](resources/mid40.gif)

- mid70

![](resources/mid70.gif)

- tele

![](resources/tele.gif)

- horizon

![](resources/horizon.gif)

## Usage

Before you write your urdf file by using this plugin, catkin_make/catkin build is needed.

A simple demo is shown in livox_simulation.launch

Run

```
    roslaunch livox_laser_simulation livox_simulation.launch
```

to see.

We can choose the lidar model by selecting different CSV file in scan_mode dir from changing the launch file:

- avia.csv
- horizon.csv
- mid40.csv
- mid70.csv
- tele.csv

## Parameters(only for display , example of avia sensor)

- laser_min_range: 0.1 // min detection range
- laser_max_range: 200.0 // max detection range
- horizontal_fov: 70.4 // °
- vertical_fov: 77.2 // °
- ros_topic: scan // name of lidar sensor topic in ROS
- samples: 24000 // number of points in each scan loop
- downsample: 1 // we can increment this parameter to decrease the consumption

### Thanks to LvFengchi and CaoMing(https://github.com/EpsAvlc) for the help of this repository！
