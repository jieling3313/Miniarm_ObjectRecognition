cmake_minimum_required(VERSION 3.0.2)
project(yolo_ros)

find_package(catkin REQUIRED COMPONENTS
  rospy
  sensor_msgs
  cv_bridge
  realsense2_camera
)

catkin_package()

install(PROGRAMS
  scripts/yolo_subscriber.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)