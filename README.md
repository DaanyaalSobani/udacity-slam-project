# udacity-slam-project

The fourth project in the [Udacity Robotics Software Engineering Nanodegree](https://www.udacity.com/course/robotics-software-engineer--nd209).

Implements Simultaneous Localisation and Mapping (SLAM) using [RTAB-Map](http://introlab.github.io/rtabmap/) (Real-Time Appearance-Based Mapping) in a simulated ROS/Gazebo environment.

## Stack

- [ROS](https://www.ros.org/) (Robot Operating System)
- [Gazebo](http://gazebosim.org/) — physics simulation
- [RTAB-Map](http://introlab.github.io/rtabmap/) — RGB-D SLAM
- `teleop_twist_keyboard` — keyboard teleoperation

## Usage

After building the catkin workspace:

```bash
source devel/setup.bash

# Launch simulation world and robot
roslaunch my_robot world.launch

# Launch RTAB-Map SLAM in a separate terminal
roslaunch main mapping.launch
```

Drive the robot around with `teleop_twist_keyboard` to build the map. The resulting 3D map and database are saved by RTAB-Map for later localisation.

## Project Structure

```
my_robot/        robot URDF and Gazebo world
rtabmap_ros/     RTAB-Map ROS integration
main/            launch files
teleop_twist_keyboard/  keyboard control node
```
