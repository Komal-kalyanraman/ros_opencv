cmake_minimum_required(VERSION 3.0.2)
project(cv_basics)

find_package(catkin REQUIRED COMPONENTS
  cv_bridge
  image_transport
  roscpp
  rospy
  sensor_msgs
  std_msgs
)

find_package( OpenCV REQUIRED)

catkin_package()

include_directories(
  ${catkin_INCLUDE_DIRS}
  ${OpenCV_INCLUDE_DIRS}
)

add_executable(webcam_pub src/webcam_pub.cpp)
target_link_libraries(webcam_pub ${catkin_LIBRARIES} ${OpenCV_LIBRARIES})

add_executable(webcam_sub src/webcam_sub.cpp)
target_link_libraries(webcam_sub ${catkin_LIBRARIES} ${OpenCV_LIBRARIES})

add_executable(webcam_rec src/webcam_rec.cpp)
target_link_libraries(webcam_rec ${catkin_LIBRARIES} ${OpenCV_LIBRARIES})