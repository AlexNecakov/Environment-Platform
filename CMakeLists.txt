cmake_minimum_required(VERSION 3.29)
project(arcadium)

set(CMAKE_PREFIX_PATH ${CMAKE_PREFIX_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/lib/cmake/sdl/lib/cmake/sdl3)

find_package(SDL3 REQUIRED CONFIG REQUIRED COMPONENTS SDL3-shared)

add_executable(arcadium main.cpp)
target_link_libraries(arcadium PRIVATE SDL3::SDL3)
