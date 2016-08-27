cmake_minimum_required(VERSION 2.8)

project( ahr_vision )

find_package( OpenCV REQUIRED )

add_executable( ahr_check CHECK_HSV.cpp )

target_link_libraries( ahr_check ${OpenCV_LIBS} )

add_executable( ahr_control "./Source/AHR/AHR_2.cpp" )

target_link_libraries( ahr_control ${OpenCV_LIBS} )

