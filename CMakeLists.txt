cmake_minimum_required(VERSION 2.8.3)
project(ros_ci)

find_package(catkin REQUIRED    
    roscpp
    rospy
    rostest
)

#just a comment
catkin_python_setup()

catkin_package(
  INCLUDE_DIRS src
)

include_directories()

if(CATKIN_ENABLE_TESTING)
  find_package(rostest REQUIRED)
  add_rostest(test/run.test)
endif()
