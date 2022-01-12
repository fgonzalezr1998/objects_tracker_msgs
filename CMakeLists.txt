cmake_minimum_required(VERSION 3.0.2)
project(objects_tracker_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  message_generation
  geometry_msgs
  std_msgs
)

add_message_files(
 FILES
 TrackerStimation.msg
 ObjectsTrack.msg
)

generate_messages(
 DEPENDENCIES
 std_msgs
 geometry_msgs
)
catkin_package(
  CATKIN_DEPENDS
  message_runtime
  std_msgs
  geometry_msgs
)