cmake_minimum_required(VERSION 3.15)
project(wx_hello)

set(CMAKE_CXX_STANDARD 20)

find_package(wxWidgets REQUIRED COMPONENTS net core base)

include(${wxWidgets_USE_FILE})

add_executable(wx_hello main.cpp)
target_link_libraries(wx_hello ${wxWidgets_LIBRARIES})