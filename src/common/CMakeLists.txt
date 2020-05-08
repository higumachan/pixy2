FILE(GLOB SOURCE_FILES src/*.cpp)

add_library(pixycommon  ${SOURCE_FILES})
target_include_directories(pixycommon PUBLIC inc)
target_include_directories(pixycommon PRIVATE ../device/libpixy_m4/inc)
target_include_directories(pixycommon PRIVATE ../device/main_m4/inc)
target_include_directories(pixycommon PRIVATE ../device/common/inc)
target_link_libraries(pixycommon /usr/local/opt/libusb/lib/libusb-1.0.0.dylib)
target_include_directories(pixycommon PRIVATE /usr/local/opt/libusb/include/libusb-1.0)
