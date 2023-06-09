# Notspot robot simulation - Python version
This repository contains all the files and code needed to simulate the notspot quadrupedal robot using [Gazebo](http://gazebosim.org/)  and [ROS](https://www.ros.org/).
The software runs on [ROS noetic](http://wiki.ros.org/noetic) and [Ubuntu 20.04](http://www.releases.ubuntu.com/20.04/). If you want to use a different ROS version, you might have to do some changes to the source code.

The robot is capable of walking.

<img src="resources/notspot_render_new1" width="233"> 
<!-- <img src="resources/notspot_render_new2" width="233"> <img src="resources/notspot_render_new3" width="233">  -->

## Setup
```
cd src && catkin_init_workspace
cd .. && catkin_make
source devel/setup.bash
roscd notspot_controller/scripts && chmod +x robot_controller_gazebo.py
cp -r RoboticsUtilities ~/.local/lib/python3.8/site-packages
roscd notspot_joystick/scripts && chmod +x ramped_joystick.py
```
## Run

In another terminal
```
source devel/setup.bash
roslaunch notspot_gazebo simulation.launch
```


## Run

In another terminal
```
source devel/setup.bash
roslaunch notspot run_robot_gazebo.launch
```

## Credits
 - mike4192: https://github.com/mike4192/spotMicro
