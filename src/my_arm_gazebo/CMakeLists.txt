cmake_minimum_required(VERSION 3.0.2)
project(my_arm_gazebo)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  gazebo_ros
  controller_manager
  joint_state_controller
  position_controllers
  transmission_interface
)

catkin_package()

install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)
install(DIRECTORY config/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/config
)
