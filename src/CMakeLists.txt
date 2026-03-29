#[[
这是一块
注释]]
cmake_minimum_required(VERSION 3.28.3)
set(SRC_LIST add.cpp sub.cpp main.cpp)
add_executable(app ${SRC_LIST})
target_include_directories(app PUBLIC .)