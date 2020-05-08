FILE(GLOB SOURCE_FILES src/*.cpp)

add_library(libpixyusb2 ${SOURCE_FILES})
target_include_directories(libpixyusb2 PUBLIC include)
target_link_libraries(libpixyusb2 pixycommon)
target_link_libraries(libpixyusb2 /usr/local/opt/libusb/lib/libusb-1.0.0.dylib)
target_include_directories(libpixyusb2 PUBLIC /usr/local/opt/libusb/include/libusb-1.0)
target_include_directories(libpixyusb2 PUBLIC ../arduino/libraries/Pixy2)

