cmake_minimum_required(VERSION 3.10)
project(solver)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
file(GLOB SOURCES "*.cpp")
if(NOT SOURCES)
message(FATAL_ERROR "No such files found in ${CMAKE_CURRENT_SOURCE_DIR}")
endif()
message(STATUS "Found sources: ${SOURCES}")
add_executable(solver ${SOURCES})
target_link_libraries(solver 
formatter_ex
solver_lib
formatter
)

