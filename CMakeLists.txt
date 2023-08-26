cmake_minimum_required(VERSION 3.0.0)
set(PROJECT_NAME ProjectCmake)
project(${PROJECT_NAME} VERSION 0.1.0 LANGUAGES C CXX)

# Setting C++ standard to 20
set(CMAKE_CXX_STANDARD 20)

# This is how we are able to simply just include 
# Ref Link: https://stackoverflow.com/questions/8304190/cmake-with-include-and-source-paths-basic-setup
include_directories(
    ${PROJECT_SOURCE_DIR}/ProjectCmake/include
    ${PROJECT_SOURCE_DIR}/ProjectCmake/src
)

# aux_source_directory(${PROJECT_SOURCE_DIR}/ProjectCmake/src all_src)

set(
    all_src
    ${PROJECT_SOURCE_DIR}/ProjectCmake/src/Box.cpp
    ${PROJECT_SOURCE_DIR}/ProjectCmake/src/Line.cpp
)

add_executable(
    ${PROJECT_NAME}
    main.cpp
    ${all_src}
)




