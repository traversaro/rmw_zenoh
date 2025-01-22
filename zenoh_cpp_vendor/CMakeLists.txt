cmake_minimum_required(VERSION 3.16)
project(zenoh_cpp_vendor)

# Default to C++17
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 17)
  set(CMAKE_CXX_STANDARD_REQUIRED ON)
endif()

find_package(ament_cmake REQUIRED)
find_package(ament_cmake_vendor_package REQUIRED)

find_package(zenohc REQUIRED)
ament_export_dependencies(zenohc)

find_package(zenohcxx REQUIRED)
ament_export_dependencies(zenohcxx)

ament_package()
