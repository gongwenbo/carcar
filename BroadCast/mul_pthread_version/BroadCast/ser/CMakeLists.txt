project(ser)
cmake_minimum_required(VERSION 2.6)
add_definitions("-Wall -g -std=c++11")
include_directories(./src ./inc )
link_directories(./)

add_subdirectory(./src)
aux_source_directory(. SRC_CODE_SER)
add_executable(ser ${SRC_CODE_SER})
target_link_libraries(ser server_lib -pthread)


