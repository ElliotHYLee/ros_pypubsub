cmake_minimum_required(VERSION 3.0.2)
project(ros_pypubsub)

find_package(catkin REQUIRED std_msgs message_generation rospy)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES pypubsub
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)

include_directories(
# include
# ${catkin_INCLUDE_DIRS}
)

catkin_install_python(PROGRAMS
  scripts/talker.py
  scripts/listener.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
