# Set target C++ standard and required compiler features
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(groundplanefit)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -std=c++11 -pthread -g -march=native")

find_package(LASlib REQUIRED)
find_package(PCL REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (ground_plane_fit main.cpp ground_plane_fitting.cpp)
target_link_libraries (ground_plane_fit
    ${PCL_LIBRARIES}
    LASlib
)
