cmake_minimum_required( VERSION 3.5)
set( CMAKE_CXX_FLAGS "-std=c++11" )

project( useLK )

# opencv
find_package(OpenCV REQUIRED)
include_directories( ${OpenCV_INCLUDE_DIRS} )

# find_package(Eigen3 REQUIRED)
# include_directories( ${Eigen3_INCLUDE_DIRS} )

# find_package(PCL REQUIRED COMPONENT common io)
# include_directories( ${PCL_INCLUDE_DIRS} )
# add_definitions( ${PCL_DEFINITIONS} )

# find_package(Sophus REQUIRED)
# include_directories( ${Sophus_INCLUDE_DIRS} )

add_executable(useLK useLK.cpp)
target_link_libraries( useLK ${OpenCV_LIBS} )
