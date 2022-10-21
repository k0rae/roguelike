cmake_minimum_required(VERSION 3.20)
project(roguelike)

set(CMAKE_CXX_STANDARD 14)

set(SDL2_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/lib/SDL/include)
set(SDL2_LIB_DIR ${PROJECT_SOURCE_DIR}/lib/SDL/lib/x86)

set(SOURCE_FILES src/main.cpp)

include_directories(${SDL2_INCLUDE_DIR})
link_directories(${SDL2_LIB_DIR})

add_executable(roguelike ${SOURCE_FILES})

target_link_libraries(roguelike SDL2main SDL2)