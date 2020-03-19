cmake_minimum_required(VERSION 3.12)

project(emptyproject NONE)

enable_language(CXX)
enable_testing()

add_subdirectory(external)
add_subdirectory(test)
