cmake_minimum_required(VERSION 3.7)
project(udp2raw_tunnel)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        lib/aes.c
        lib/md5.c
        common.cpp
        encrypt.cpp
        log.cpp
        main.cpp
        network.cpp
        )
set(CMAKE_CXX_FLAGS "-Wall -Wextra -Wno-unused-variable -Wno-unused-parameter -static")
set(CMAKE_LINK_LIBRARY_FLAG "-lrt")
add_executable(udp2raw_tunnel ${SOURCE_FILES})