cmake_minimum_required(VERSION 3.19)
project(main)

set(CMAKE_CXX_STANDARD 14)

link_directories(cmake-build-debug/extern_lib/glfw/src)
add_subdirectory(extern_lib/glfw)

include_directories(include)
include_directories(extern_lib/glfw/include)

add_executable(main main.cpp src/glad.c)

target_link_directories(main PUBLIC glfw)

target_link_libraries(main glfw3)