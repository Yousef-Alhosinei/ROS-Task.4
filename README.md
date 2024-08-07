# ROS-Task.4
# ROS foxy

method to control the Turtlesim turtle by publishing velocity commands directly to the /turtle1/cmd_vel topic:

# 1.Install the Turtlesim package:


sudo apt install ros-foxy-turtlesim

# 2.Initialize ROS:


source /opt/ros/foxy/setup.bash

# 3.Launch the Turtlesim Node:


roscore
In another terminal:


source /opt/ros/foxy/setup.bash
ros2 run turtlesim turtlesim_node

# 4.Publish Velocity Commands:
Open another terminal, initialize ROS, and use this command to move the turtle:


source /opt/ros/foxy/setup.bash
ros2 topic pub /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0, y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 1.8}}"
This will allow you to control the turtle by sending velocity commands directly.
