cmake_minimum_required(VERSION 3.22 FATAL_ERROR)
project(gstreamer VERSION 1.0.0 LANGUAGES C)

find_package(PkgConfig REQUIRED)
pkg_search_module(gstreamer REQUIRED IMPORTED_TARGET gstreamer-1.0>=1.4)
pkg_check_modules(gstreamer-audio REQUIRED IMPORTED_TARGET gstreamer-audio-1.0)
pkg_check_modules(gstreamer-pbutils REQUIRED IMPORTED_TARGET gstreamer-pbutils-1.0)
pkg_check_modules(gtk REQUIRED IMPORTED_TARGET gtk+-3.0)

add_subdirectory(src)
