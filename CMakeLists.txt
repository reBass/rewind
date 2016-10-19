cmake_minimum_required(VERSION 3.2)
project(rewind)

set(CMAKE_CXX_STANDARD 14)

find_package(Qt5 REQUIRED COMPONENTS Core Widgets Gui)
add_subdirectory(external/rtaudio EXCLUDE_FROM_ALL)

set(SOURCE_FILES src/main.cpp)
add_executable(rewind ${SOURCE_FILES})
target_link_libraries(rewind rtaudio)
target_link_libraries(rewind Qt5::Core Qt5::Gui Qt5::Widgets)
