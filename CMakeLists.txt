cmake_minimum_required( VERSION 2.8.11 )

if( NOT MSVC )
    add_definitions( -std=c++11 )
endif()

file( GLOB SOURCE_FILES RELATIVE ${CMAKE_CURRENT_SOURCE_DIR}
    [^.]*.cpp
    [^.]*.h
    )

add_library( nah STATIC ${SOURCE_FILES} )
set_target_properties( nah PROPERTIES POSITION_INDEPENDENT_CODE ON )
