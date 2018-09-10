cmake_minimum_required(VERSION 3.12)
project(skia_test)

set(CMAKE_CXX_STANDARD 11)

set(SKIA_HOME /media/program/linux/work/git/skia/skia)

include_directories(
        ${SKIA_HOME}/include
        ${SKIA_HOME}/include/android
        ${SKIA_HOME}/include/atlastext
        ${SKIA_HOME}/include/c
        ${SKIA_HOME}/include/codec
        ${SKIA_HOME}/include/config
        ${SKIA_HOME}/include/core
        ${SKIA_HOME}/include/effects
        ${SKIA_HOME}/include/encode
        ${SKIA_HOME}/include/gpu
        ${SKIA_HOME}/include/pathops
        ${SKIA_HOME}/include/ports
        ${SKIA_HOME}/include/private
        ${SKIA_HOME}/include/svg
        ${SKIA_HOME}/include/utils
)

link_libraries(SDL2 SDL2main /media/program/linux/work/git/skia/skia/out/Shared/libskia.so)

add_executable(skia_test main.cpp)