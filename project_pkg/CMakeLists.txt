cmake_minimum_required(VERSION 3.0.2)
project(project_pkg)


find_package(catkin REQUIRED COMPONENTS
  roscpp
  roslib
  geometry_msgs
  mavros_msgs
)

catkin_package(
    CATKIN_DEPENDS roscpp roslib geometry_msgs mavros_msgs
    )

include_directories(
  include ${catkin_INCLUDE_DIRS}
)

add_executable(offboard_node src/offboard_node.cpp)
target_link_libraries(offboard_node ${catkin_LIBRARIES})


