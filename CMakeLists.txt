cmake_minimum_required(VERSION 3.17)

set(LIB_ROOT_DIR ${CMAKE_SOURCE_DIR}/3rdParty)

project("vEngine")

if(MSVC)
    add_definitions(-D_CTR_SECURE_NO_WARNINGS)
endif()

add_subdirectory("vEngine")
