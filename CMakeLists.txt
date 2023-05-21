cmake_minimum_required(VERSION 3.25)
project(3dgame)

set(CMAKE_CXX_STANDARD 17)

add_executable(3dgame src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw-3.3.8)
add_subdirectory(external/glad)
target_link_libraries(3dgame glfw glad)
