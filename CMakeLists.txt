cmake_minimum_required(VERSION 3.13)
project(keynav C)

set(CMAKE_C_STANDARD 11)

add_definitions (-D_GNU_SOURCE)

include_directories(
    .
    /usr/include/cairo
    /usr/include/glib-2.0
    /usr/lib/x86_64-linux-gnu/glib-2.0/include
    /usr/include/pixman-1
    /usr/include/freetype2
    /usr/include/libpng12
    /usr/include/glib-2.0
    /usr/lib/x86_64-linux-gnu/glib-2.0/include
)

add_executable(keynav
    keynav.c
    keynav_version.h)
target_link_libraries (keynav cairo X11 Xext Xinerama glib-2.0  xdo)