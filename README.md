# Taylor-Robot

**Taylor** is a differential robot built using **ROS2**.
<p align="middle">
  <img src="/docs/taylor_hd1.jpg" style="height: 40%; width: 40%"/> 
  <img src="/docs/taylor_hd2.jpg" style="height: 40%; width: 40%"/> 
  <img src="/docs/taylor_hd3.jpg" style="height: 40%; width: 40%"/> 
  <img src="/docs/taylor_hd4.jpg" style="height: 40%; width: 40%"/> 
</p>



# ros2_control <img src="/docs/logo_ros-controls.png" width="30px" height="30px"/> 

[ros2_control](https://control.ros.org/master/index.html) package is used to control the two wheels. The **Arduino Nano** is used as a hardware component that receives a command from controllers and converts it to a PWM signal for the H bridge, through the Arduino Nano the controllers can read/write to these interfaces.

It is the **Raspberry Pi B+** that runs the controllers, which compares the reference value with the measurement output from the encoders and calculates the system's input based on this error (for more details, visit [Control Theory](https://en.wikipedia.org/wiki/Control_theory)).

# Nav2 <img src="https://aws1.discourse-cdn.com/business7/uploads/ros/original/2X/7/781fa8ce870432b9682a95f855b315c454da87c7.png" width="30" height="54"/>

The **Nav2** package allows mobile robots to move safely from one location to another. Using sensors, this package performs mapping, localization, and perception functions. In addition to collecting information about the environment, these sensors can be used to build and maintain a map of the environment, to pinpoint the robot on the map, and to avoid obstacles that may be encountered in that environment.

**LIDAR** (RPLIDAR A1) and **encoders** from the wheels are used as sensors for this project, so Taylor can navigate on his own in a mapped world using Nav2.

# How to setup
