cmake_minimum_required(VERSION 3.22)
project(race)
set (CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}) 
set (CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})
include_directories(lib)
add_subdirectory(lib)
add_executable(race main.cpp)
find_library(SOURCE_DLL race_dll ./lib)
target_link_libraries(race race_dll)