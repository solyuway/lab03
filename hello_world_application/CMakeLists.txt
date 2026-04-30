cmake_minimum_required(VERSION 3.10)
project(hello_world)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
file(GLOB SOURCES "*.cpp")
if(NOT SOURCES)
message(FATAL_ERROR "No such files found in ${CMAKE_CURRENT_SOURCE_DIR}")
endif()
message(STATUS "Found sources: ${SOURCES}")
add_executable(hello_world ${SOURCES})
target_link_libraries(hello_world 
formatter_ex
formatter
)
