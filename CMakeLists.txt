cmake_minimum_required(VERSION 3.10)
PROJECT(uSockets)
set(CMAKE_INSTALL_PREFIX "/usr/")
set(CMAKE_DEBUG_POSTFIX "d")
set(CMAKE_BUILD_TYPE "Release")
include_directories(src)
AUX_SOURCE_DIRECTORY(./src/ DIR_SRCS)
AUX_SOURCE_DIRECTORY(./src/eventing/ DIR_SRCS)
ADD_LIBRARY(uSockets SHARED ${DIR_SRCS})

