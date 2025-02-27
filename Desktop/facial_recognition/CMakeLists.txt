cmake_minimum_required(VERSION 3.10)
project(FaceDetection)

# Manually specify OpenCV installation path
set(OpenCV_DIR /opt/homebrew/Cellar/opencv/4.11.0_1/share/opencv4)

find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})
link_directories(${OpenCV_LIB_DIR})

add_executable(FaceDetection facedetect.cpp)
target_link_libraries(FaceDetection ${OpenCV_LIBS})
