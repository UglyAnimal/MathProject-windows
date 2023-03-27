cmake_minimum_required(VERSION 3.26.1)
project(MathProject)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

add_library(MathLibrary STATIC src/MathLibrary.cpp)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

add_executable(MathClient src/MathClient.cpp)
target_link_libraries(MathClient MathLibrary)