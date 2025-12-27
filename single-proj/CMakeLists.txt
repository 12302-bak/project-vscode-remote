cmake_minimum_required(VERSION 3.10)

project(single_proj C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_BUILD_TYPE Debug)

add_compile_options(-g)

include_directories(${PROJECT_SOURCE_DIR}/include)
file(GLOB SRC_LIST "${CMAKE_CURRENT_SOURCE_DIR}/src/*.c")
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

# add_library(calc SHARED ${SRC_LIST})
add_executable(calc calc.c ${SRC_LIST})