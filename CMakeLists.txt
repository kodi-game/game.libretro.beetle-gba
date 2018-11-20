cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-gba)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(BEETLE-GBA_LIB NAMES mednafen_gba_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(BEETLE-GBA_CUSTOM_BINARY ${BEETLE-GBA_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE-GBA "")

include(CPack)
