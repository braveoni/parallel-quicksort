cmake_minimum_required(VERSION 3.22)
project(parallel_quicksort)

set(CMAKE_CXX_STANDARD 20)

add_executable(parallel_quicksort main.cpp)

MATH(EXPR stack_size "512 * 1024 * 1024") # 16 Mb
set(CMAKE_EXE_LINKER_FLAGS "-Wl,--stack,${stack_size}")