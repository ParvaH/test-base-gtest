


#    Filename : CmakeLists.txt
# Description : Definition of all source and header files of one package.
#               To add this package to a project, include this file in the corresponding CMakeLists.txt file.
#      Author :
#     Release :
#   Copyright : 
#    Revision : 
# ------------------------------------------------------------------------------------------------
#     History : 
# ================================================================================================
cmake_minimum_required (VERSION 3.7)

project(TestBase)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14")

find_package(Boost REQUIRED COMPONENTS program_options)
include_directories(${Boost_INCLUDE_DIR})

add_executable(TestBase
                app/main.cpp
                src/library.cpp
)

include_directories(
                src/
                app/
)

# link Boost libraries to the new target
target_link_libraries(TestBase ${Boost_LIBRARIES})
