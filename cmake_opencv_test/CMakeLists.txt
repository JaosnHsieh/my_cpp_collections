cmake_minimum_required(VERSION 2.8)
project (find_package_learning)
find_package( OpenCV REQUIRED )

message (STATUS "OpenCV_ DIR = ${OpenCV_DIR}")
message (STATUS "OpenCV_INCLUDE_DIRS = ${OpenCV_INCLUDE_DIRS}")
message (STATUS "OpenCV_ LIBS = ${OpenCV_LIBS}")

include_directories (${OPENCV_INCLUDE_DIRS})
add_executable (opencv_test opencv_test.cpp)
target_link_libraries(opencv_test ${OpenCV_LIBS})