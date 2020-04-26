cmake_minimum_required(VERSION 3.15)
project(wx_hello)

set(wxBUILD_SHARED FALSE)
set(CMAKE_CXX_STANDARD 17)

# Mac OSX Bundle Properties
set(MACOSX_BUNDLE_NAME "My Application")
set(MACOSX_BUNDLE_PACKAGE_NAME "rangeli.myapp")

add_subdirectory(libs/wxWidgets)
add_executable(wx_hello main.cpp)
set_target_properties(wx_hello PROPERTIES
        MACOSX_BUNDLE ON
        MACOSX_BUNDLE_INFO_PLIST ${CMAKE_CURRENT_SOURCE_DIR}/MacOSXBundleInfo.plist.in)
target_link_libraries(wx_hello net core base)