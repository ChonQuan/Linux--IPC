cmake_minimum_required(VERSION 3.0.0)
project(Linux-IPC VERSION 0.1.0)

set(LIBRARY_OUTPUT_PATH    ${CMAKE_BINARY_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)
set(LIBIPC_PROJECT_DIR     ${PROJECT_SOURCE_DIR})

add_subdirectory(src)
add_subdirectory(test)
