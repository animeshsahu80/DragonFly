# DragonFly
Software Setup for Outdoor UAV at RRC-IIIT Hyderabad

![Hardware Map](/extras/hardware.png)

## Installation
_**NOTE:** Please run this installation only on a fresh formatted system with Ubuntu 16/18_

```
git clone https://github.com/harshitsankhla/DragonFly.git
cd DragonFly
sudo chmod +x drone.sh
. drone.sh
```

## Manual Changes
_**1. Set your Monocular Camera Serial Number**_<br/>
In file = ~/dragonfly_ws/src/bluefox2/launch/single_node.launch : <arg name="device" default="**ENTER_SERIAL_HERE**"/> 

_**2. Set your Image and IMU topic for VINS-Mono**(verify exact names by running - rostopic list)_<br/>
In file = ~/dragonfly_ws/src/VINS-Mono/config/bf_xsens/bf_xsens_config.yaml

## Tips and Tricks
_**1. Command for Static Transform Publish between frames (will be used for attaching other sensor frames to odometry frame)**_
```
rosrun tf static_transform_publisher x y z yaw pitch roll parent_frame child_frame period_in_ms
```

GDrive - https://drive.google.com/open?id=1M_KefI5scPEAR6IHr5KD8DPDBbuKsVKl
