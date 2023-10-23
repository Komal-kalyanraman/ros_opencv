# About
This is a common workspace for various opencv packages

## Make sequence for cv_basics package
1. Create build, devel folders next to build folder.
2. Run "catkin_make" in at catkin_ws/
3. Then do a source devel/setup.bash
4. Run "roslaunch cv_basics cv_basics_cpp.launch" to run both nodes of cv_basics package.
5. To run a specific node, run "rosrun cv_basics webcam_pub"
6. To display published image, run "rosrun image_view image_view image:=/camera"

reference link: https://automaticaddison.com/working-with-ros-and-opencv-in-ros-noetic/

