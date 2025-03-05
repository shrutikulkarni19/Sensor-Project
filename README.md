
In this project, PID control and image processing methods are used to create an autonomous racing vehicle control system. The system reads real-time video inputs to identify track boundaries and dynamically compute steering adjustments, all while utilizing the ROS 2 Foxy framework. Key responsibilities include using morphological processes to improve picture quality for line recognition and adjusting HSV color (green) ranges to different light levels for reliable track detection.

Based on the perceived deviation from the track center, a PID controller determines the required steering changes, combining error integration and distinction for responsive and smooth vehicle control. In order to dynamically modify the car's speed for the best possible racing performance, the system also computes the track's curvature based on lines that are identified.


## How to Run
After ensuring that all components are set up and all prerequisites have been installed, follow these steps to run the system (All on seprate terminals):
1. Launch the arc_startup file containing the startups for the camera and vesc_driver package.
	- Command: _`ros2 launch arc_startup startup.launch.py`_
2. Launch the vesc_ackermann package for command translation.
	- Command: _`ros2 launch vesc_ackermann ackermann_to_vesc_node.launch.xml`_
3. Finally, once these two launch files are successfully launched, start the autonomous algorithm package.
	- Command: _`ros2 launch arc_autonomous_ctrl autonomous_ctrl.launch.py`_


