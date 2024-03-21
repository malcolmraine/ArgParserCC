###############################################################################
# File: CMakeLists.txt
# Description:
# Author: Malcolm Hall
# Date: 3/20/24
# Version: 1
#
###############################################################################

file(GLOB source_files ${CMAKE_CURRENT_LIST_DIR}/*.cpp)
file(GLOB include_files ${CMAKE_CURRENT_LIST_DIR}/*.h)
list(APPEND SOURCES ${source_files})
list(APPEND INCLUDES ${include_files})

ADD_LIBRARY(ALIB_ARGPARSERCC STATIC ${SOURCES})