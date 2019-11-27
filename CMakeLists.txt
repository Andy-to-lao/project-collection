cmake_minimum_required(VERSION 2.8.3)
project(test)
add_compile_options(-std=c++11 -O0 -g)
find_package(OpenCV 3.4.5 REQUIRED)

add_executable(testcv 
  src/calibrate.cpp
  src/CameraCalibrator.cpp
)
target_link_libraries(testcv
  ${OpenCV_LIBS}
)

