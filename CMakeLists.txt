cmake_minimum_required(VERSION 3.16)

project(hello_home)

add_subdirectory(lib)
add_subdirectory(bin)

enable_testing()

add_test(test-static hello-lib-static)
add_test(test-dynamic hello-lib-dynamic)

