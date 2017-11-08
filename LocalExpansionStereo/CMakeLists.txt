

project(LocalExpansionStereo)
cmake_minimum_required(VERSION 2.8)
set(CMAKE_BUILD_TYPE "Release")
#set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake")

#include_directories(${CMAKE_CURRENT_SOURCE_DIR})   

find_package( OpenCV REQUIRED )
if( OpenCV_FOUND )
list( APPEND ThirdParty_LIBS ${OpenCV_LIBS} )
    include_directories( ${OpenCV_INCLUDE_DIRS} )
endif( OpenCV_FOUND )