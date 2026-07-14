---
name: ros-dev
---

# ROS 2 Development Guide

## When to use

* Create a new ROS 2 node or package
* Refactoring ROS 2 nodes

## Core Pattern

* When building a ROS 2 node, decouple the core logic from the ROS 2 side of the code
* The core logic should have minimal ROS 2 dependencies
* The "interface" to the node is the topics, servies and actions, that should be decoupled from the core logic
* Thoroughly unit test the core logic
* The core logic should compiled into it's own library

## ROS 2 Feature Preferences

* Use rclcpp component nodes for C++ nodes. Use the EXECUTABLE arguement when registering as to not require a main.cpp



