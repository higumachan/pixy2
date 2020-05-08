cmake_minimum_required(VERSION 3.16)
project(pixy)

add_definitions(-DCORE_M4)

add_subdirectory(src/common)
add_subdirectory(src/host/libpixyusb2)
add_executable(get_rgb_demo src/host/libpixyusb2_examples/get_rgb_demo/get_rgb_demo.cpp)
target_link_libraries(get_rgb_demo libpixyusb2)
target_include_directories(get_rgb_demo PUBLIC /usr/local/opt/libusb/include/libusb-1.0)
