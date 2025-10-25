cmake_minimum_required(VERSION 3.16)

project(opusfile)

add_subdirectory(third_party)

add_library(opusfile
    src/info.c
    src/internal.c
    src/internal.h
    src/opusfile.c
    src/stream.c
    src/winerrno.h
    include/opusfile.h
)

target_include_directories(opusfile PUBLIC include)
target_link_libraries(opusfile PRIVATE ogg opus)