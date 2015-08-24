project(game.libretro.beetle-gba)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(beetle-gba REQUIRED)

set(DEPLIBS meteor)
set(BEETLE_GBA_CUSTOM_BINARY ${BEETLE_GBA_LIB}
                             game.libretro.beetle-gba${CMAKE_SHARED_LIBRARY_SUFFIX} beetle-gba)

build_addon(game.libretro.beetle-gba BEETLE_GBA DEPLIBS)
