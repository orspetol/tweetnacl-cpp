cmake_minimum_required(VERSION 2.8)


set(EXECUTABLE_OUTPUT_PATH   ${CMAKE_BINARY_DIR}/bin)
set(RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(LIBRARY_OUTPUT_PATH      ${CMAKE_BINARY_DIR}/lib)

project(TweetNaCl)

file(GLOB h src/*.h)
file(GLOB c src/*.c)
file(GLOB cpp src/*.cpp)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${fpic} -std=c++14 -Wall -Wextra")


add_library(tweetnacl   STATIC ${h} ${c})
add_library(tweetnacl++ STATIC ${h} ${cpp})

