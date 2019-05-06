# Scissor-lift-IDE
Code for controlling a scissor lift with ROS and Arduino
Before running the code make sure the lift has a voltage input of 23V and the arduino is connected to your PC.

Steps to get the code running:

1) Open a new Terminal on Linux
  --> adruino
2) Open a new Terminal on Linux
  --> run roscore
3) Open a new Terminal on Linux
  --> rosrun rosserial_python serial_node.py /dev/ "USB port on which the arduino is running" (e.g ttyUSB0)
