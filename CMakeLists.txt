cmake_minimum_required(VERSION 3.6)
project(rewind)

set(CMAKE_CXX_STANDARD 14)

find_package(Qt5 REQUIRED COMPONENTS Core Widgets Gui)

set(SOURCE_FILES main.cpp)
add_executable(rewind ${SOURCE_FILES})
target_link_libraries(rewind Qt5::Core Qt5::Gui Qt5::Widgets)
