cmake_minimum_required(VERSION 2.8)
project(dense_trajectory_release_v1_2)

find_package(OpenCV REQUIRED core imgproc highgui)

include_directories(${OpenCV_INCLUDE_DIRS})


set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES DenseTrack.cpp)
add_executable(dense_trajectory_release_v1_2 ${SOURCE_FILES})
target_link_libraries(dense_trajectory_release_v1_2 ${OpenCV_LIBS})