cmake_minimum_required(VERSION 3.10)
project(MinecraftClone)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra")
add_definitions(-DMY_MACRO)


find_package(SDL2 REQUIRED)
find_package(OpenGL REQUIRED)

include_directories(include)

add_executable(MinecraftClone src/main.cpp)
target_link_libraries(MinecraftClone SDL2 OpenGL::OpenGL)

