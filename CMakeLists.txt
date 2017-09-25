cmake_minimum_required(VERSION 3.7)
project(demo)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        main.cpp
        old_main.cpp
        VideoFaceDetector.cpp
        VideoFaceDetector.h)

add_executable(demo ${SOURCE_FILES})