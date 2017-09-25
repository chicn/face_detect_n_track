cmake_minimum_required(VERSION 3.7)
project(demo)

set(CMAKE_CXX_STANDARD 11)

file(COPY haarcascade_frontalface_default.xml DESTINATION ${PROJECT_SOURCE_DIR}/cmake-build-release)

set(SOURCE_FILES
        main.cpp
        VideoFaceDetector.cpp
        VideoFaceDetector.h)

# OpenCV
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(demo ${SOURCE_FILES})

target_link_libraries(demo ${OpenCV_LIBS})
