cmake_minimum_required(VERSION 3.6)
project(trackingv2)

find_package( OpenCV )
include_directories( ${OpenCV_INCLUDE_DIRS} )
set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES tracking.cpp featuretracker.h videoprocessor.h)
add_executable(trackingv2 ${SOURCE_FILES})

target_link_libraries( trackingv2 ${OpenCV_LIBS} )