cmake_minimum_required(VERSION 3.1)

# set the project name
project(TFLiteInference)

# Enable C++11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)
set(CMAKE_PREFIX_PATH /home/anhph/OpenCV)
find_package(OpenCV REQUIRED)
include_directories( ${OpenCV_INCLUDE_DIRS})

# add the executable
add_executable(TFLiteInference tflite_inference.cpp)
target_link_libraries(TFLiteInference ${OpenCV_LIBS})