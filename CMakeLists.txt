cmake_minimum_required(VERSION 3.26)

set(PROJECT_NAME couriers)
project(${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 17)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_executable(${PROJECT_NAME} main.cpp)
add_subdirectory(external/glfw)
target_link_libraries(${PROJECT_NAME} glfw)
