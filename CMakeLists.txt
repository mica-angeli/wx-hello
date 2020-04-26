cmake_minimum_required(VERSION 3.15)
project(wx_hello)

set(wxBUILD_SHARED FALSE)
set(CMAKE_CXX_STANDARD 17)

add_subdirectory(libs/wxWidgets)
add_executable(wx_hello main.cpp)
target_link_libraries(wx_hello net core base)