cmake_minimum_required (VERSION 3.15)

project ("libiconv")
set (CMAKE_CXX_STANDARD 20)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)

set(SOURCES 
        ${CMAKE_CURRENT_SOURCE_DIR}/libiconv/iconv.c
        ${CMAKE_CURRENT_SOURCE_DIR}/libiconv/localcharset.c
        ${CMAKE_CURRENT_SOURCE_DIR}/libiconv/relocatable.c
        )
		
add_library(libiconv SHARED ${SOURCES})
target_include_directories(libiconv PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)
