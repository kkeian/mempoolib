cmake_minimum_required(VERSION 3.22.1)
project(mempoolib)
set(CMAKE_DEBUG_POSTFIX dbg)

add_executable(hello src/main.cxx)
# static lib
add_library(mempoolib src/mempoolib.cxx)
set_target_properties(mempoolib PROPERTIES DEBUG_POSTFIX ${CMAKE_DEBUG_POSTFIX})
# dynamic/shared lib - uncomment if you prefer shared
#add_library(mempoolib SHARED mempoolib.cxx)