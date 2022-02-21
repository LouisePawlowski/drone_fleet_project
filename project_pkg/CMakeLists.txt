cmake_minimum_required(VERSION 3.0.2)
project(project_pkg)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_STANDARD 17)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  roslib
  geometry_msgs
  mavros_msgs
)

find_package(catkin REQUIRED)

add_executable(main src/main.cpp)


