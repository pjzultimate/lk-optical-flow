cmake_minimum_required(VERSION 2.8)
project(optical)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
#Eigen
INCLUDE_DIRECTORIES("usr/include/eigen3")
find_package(OpenCV 3.3.0 REQUIRED)
INCLUDE_DIRECTORIES(${OpenCV_INCLUDE_DIRS})
ADD_EXECUTABLE(GL optical_flow.cpp)
target_link_libraries(GL ${OpenCV_LIBS})


