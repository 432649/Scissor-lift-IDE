# Scissor-lift-IDE
Code for controlling a scissor lift with ROS and Arduino
Before running the code make sure the lift controler has a voltage input of 23V and the arduino is connected to your PC.

Steps to get the code running (--> means type ...):

1) Open a new Terminal on Linux (start the Arduino IDE)
  --> adruino
2) Open a new Terminal on Linux (start roscore)
  --> run roscore
3) Open a new Terminal on Linux (launch a ros node)
  --> rosrun rosserial_python serial_node.py /dev/ "USB port on which the arduino is running" (e.g ttyUSB0)
4) Open a new Terminal on Linux (run the first publisher which controls the speed of the lift)
  --> rostopic pub -1 topic messagetype -- "value from -
  --> rostopic pub -1 robobarista/linear_motors_speed std_msgs/UInt16 -- "value from 0-255"
5) Open a new Terminal on Linux (run the second publisher which controls the height of the lift)
  --> rostopic pub -1 topic messagetype -- "value from 0-70cm"
  --> rostopic pub -1 /robobarista/height_input std_msgs/UInt8 -- "value from 0-70cm" 
  
