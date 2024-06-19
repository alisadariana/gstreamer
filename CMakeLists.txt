cmake_minimum_required(VERSION 3.0.0)
project(gstreamer VERSION 0.1.0 LANGUAGES C)

find_package(PkgConfig REQUIRED)
pkg_search_module(gstreamer REQUIRED IMPORTED_TARGET gstreamer-1.0>=1.4)

add_executable(basic-tutorial-1
        basic-tutorial-1.c)

target_link_libraries(basic-tutorial-1
    PkgConfig::gstreamer
)
