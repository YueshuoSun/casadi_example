cmake_minimum_required(VERSION 3.10)

project(CasadiExample CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(casadi_example casadi_example.cc)

find_library(CASADI_LIBRARY casadi PATHS /usr/local/lib)
target_link_libraries(casadi_example ${CASADI_LIBRARY})
