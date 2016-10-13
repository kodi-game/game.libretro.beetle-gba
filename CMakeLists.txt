cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-gba)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-beetle-gba REQUIRED)

set(DEPLIBS meteor)
set(BEETLE_GBA_CUSTOM_BINARY ${BEETLE_GBA_LIB}
                             ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE_GBA DEPLIBS)
