###############################################################################
# File: CMakeLists.txt
# Description:
# Author: Malcolm Hall
# Date: 3/20/24
# Version: 1
#
###############################################################################
SET(PROJECT_NAME ArgParserCC_ExampleShowHelp)
cmake_minimum_required(VERSION 3.20)
project(${PROJECT_NAME})
set(CMAKE_CXX_STANDARD 20)

###############################################################################
###############################################################################

include(../../src/CMakeLists.txt)
SET( TARGET ${PROJECT_NAME} )

add_executable(${TARGET} main.cpp)
target_link_libraries( ${TARGET} ALIB_ARGPARSERCC)

if (CMAKE_BUILD_TARGET EQUAL "Release" OR CMAKE_BUILD_TARGET EQUAL "Test")
    target_compile_options(${TARGET} PUBLIC -Werror -o3)
elseif(CMAKE_BUILD_TARGET EQUAL "Debug")
    target_compile_options(${TARGET} PUBLIC -Werror -o1)
endif()

###############################################################################
###############################################################################
