cmake_minimum_required(VERSION 3.22)
project(hello-lib CXX)

add_library(hello-lib-static STATIC include/hello_world_lib.h source/hello_world_lib.cpp)
target_include_directories(hello-lib-static
                           PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_compile_features(hello-lib-static PUBLIC cxx_std_20)

add_library(hello-lib-dynamic SHARED include/hello_world_lib.h source/hello_world_lib.cpp)
target_include_directories(hello-lib-dynamic
                           PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_compile_features(hello-lib-dynamic PUBLIC cxx_std_20)


