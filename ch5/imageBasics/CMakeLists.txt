cmake_minimum_required( VERSION 2.8)
set( CMAKE_CXX_FLAGS "-std=c++11" )

project( imageBasics )

find_package(OpenCV REQUIRED)
include_directories( ${OpenCV_INCLUDE_DIRS} )

# find_package(Eigen3 REQUIRED)
# include_directories( ${Eigen3_INCLUDE_DIRS} )

# find_package(Sophus REQUIRED)
# include_directories( ${Sophus_INCLUDE_DIRS} )

add_executable(imageBasics imageBasics.cpp)
target_link_libraries( imageBasics ${OpenCV_LIBS} )
