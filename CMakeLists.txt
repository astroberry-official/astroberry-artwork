cmake_minimum_required(VERSION 2.8)
PROJECT(astroberry-artwork NONE)

set (VERSION_MAJOR 3)
set (VERSION_MINOR 0)

set(ARTWORK_DIR "/usr/share")

if (${CMAKE_SYSTEM_NAME} MATCHES "Linux")
        install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/astroberry-artwork DESTINATION ${ARTWORK_DIR})
endif()
