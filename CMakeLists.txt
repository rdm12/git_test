cmake_minimum_required(VERSION 2.8)
set(target testlib)
project(${target})

ADD_LIBRARY( foo SHARED
  src/foo.cpp
)

add_executable(${target} src/main.cpp)

target_link_libraries(${target} foo)