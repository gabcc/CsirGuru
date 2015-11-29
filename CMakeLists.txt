cmake_minimum_required(VERSION 3.3)
project(csirguru)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

find_package(OpenGL REQUIRED)
include_directories(${OPENGL_INCLUDE_DIR})

find_package(GLUT REQUIRED)
include_directories(${GLUT_INCLUDE_DIR})


set(SOURCE_FILES main.cpp)
add_executable(csirguru ${SOURCE_FILES})

target_link_libraries(csirguru ${OPENGL_LIBRARIES} ${GLUT_LIBRARIES})