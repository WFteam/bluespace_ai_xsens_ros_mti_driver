#
# Copyright © 2023 Glydways, Inc.
# https://glydways.com/
#

# Default to C++14
# set(CMAKE_CXX_STANDARD 14)
# set(CXX_STANDARD 14)
# # set(CMAKE_CXX_STANDARD 14)
# set(CMAKE_CXX_STANDARD_REQUIRED ON)
# set(C_FLAG_CACHE ${CMAKE_C_FLAGS})
# set(CXX_FLAG_CACHE ${CMAKE_CXX_FLAGS})
# set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wno-error")
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wno-error")
# add_compile_options(
#     $<$<COMPILE_LANGUAGE:C>:-Wno-error>
#     $<$<COMPILE_LANGUAGE:CXX>:-Wno-error>
# )

# add_definitions(-w)

set(XSPUBLIC_COMPILE_OPTIONS "-w")

file(GLOB XSPUBLIC_HEADERS
    "xscommon/*.h"
    "xscontroller/*.h"
    "xstypes/*.h"
    )



file(GLOB XSPUBLIC_SOURCES
    "xscontroller/*.c"
    "xscontroller/*.cpp"
    "xscommon/*.c"
    "xscommon/*.cpp"
    "xstypes/*.c"
    "xstypes/*.cpp"
    )

set(CMAKE_INCLUDE_CURRENT_DIR ON)

glyd_add_library(
    xsens_mt
    ALIAS
        third_party::xsens_mt
    HEADERS
        ${XSPUBLIC_HEADERS}
    SOURCES
        ${XSPUBLIC_SOURCES}
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}
    COMPILE_OPTIONS
        ${XSPUBLIC_COMPILE_OPTIONS}
    )
