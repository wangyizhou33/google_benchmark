# Specify the minimum version of CMake required
cmake_minimum_required(VERSION 3.10)

# Set the project name
project(MyProject)

find_package(benchmark REQUIRED)

# Add an executable target
add_executable(my_executable main.cpp)
target_link_libraries(my_executable benchmark::benchmark)
