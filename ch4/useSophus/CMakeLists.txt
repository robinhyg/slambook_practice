cmake_minimum_required( VERSION 2.8)

project( useSophus )

find_package(Eigen3 REQUIRED)
include_directories( ${Eigen3_INCLUDE_DIRS} )

find_package(Sophus REQUIRED)
include_directories( ${Sophus_INCLUDE_DIRS} )

add_executable(useSophus useSophus.cpp)
target_link_libraries( useSophus ${Sophus_LIBRARIES} )
