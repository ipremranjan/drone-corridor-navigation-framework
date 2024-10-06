cmake_minimum_required(VERSION 3.0.2)
project(drone_corridor)

set(CMAKE_PREFIX_PATH ${CMAKE_PREFIX_PATH} "/opt/ros/humble")
set(catkin_DIR "/opt/ros/humble/share/catkin/cmake/catkin")

find_package(catkin REQUIRED COMPONENTS
  rospy
  gazebo_ros
)

catkin_package(
  CATKIN_DEPENDS rospy gazebo_ros
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install(DIRECTORY launch models
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)