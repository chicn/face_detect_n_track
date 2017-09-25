cmake_minimum_required(VERSION 3.7)
project(demo)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        main.cpp
        old_main.cpp
        VideoFaceDetector.cpp
        VideoFaceDetector.h)

# OpenCV
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(demo ${SOURCE_FILES})

target_link_libraries(demo ${OpenCV_LIBS})