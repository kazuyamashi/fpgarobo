cmake_minimum_required(VERSION 2.8.3)
project(fpgarobo)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  sensor_msgs
  std_msgs
  rospy
  message_generation
)

# Generate messages in the 'msg' folder
add_message_files(
  FILES
  FpgaroboMsg.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  sensor_msgs
  std_msgs
)

catkin_package(
  # INCLUDE_DIRS include
  LIBRARIES sample
  CATKIN_DEPENDS roscpp rospy sensor_msgs std_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

# add_executable(fpgarobo src/fpgarobo.cpp)
# target_link_libraries(fpgarobo ${catkin_LIBRARIES})