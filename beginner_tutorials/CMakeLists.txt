cmake_minimum_required(VERSION 3.0.2)
project(beginner_tutorials)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
)

catkin_package()

include_directories(include ${catkin_INCLUDE_DIRS})

add_executable(talker scripts/talker.cpp)
target_link_libraries(talker ${catkin_LIBRARIES})


add_executable(receiver scripts/receiver.cpp)
target_link_libraries(receiver ${catkin_LIBRARIES})