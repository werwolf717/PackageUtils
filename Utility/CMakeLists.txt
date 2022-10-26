cmake_minimum_required(VERSION 3.0)

#Settings
set(PROJECT_NAME PackageUtilitiesApp)
set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
set(INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)

#find libs
find_library(HELLO_LIB libhello.so)
message(STATUS ${HELLO_LIB})

#assembly
add_executable(${PROJECT_NAME} ${SRC_DIR}/Main.cpp)
target_link_libraries(${PROJECT_NAME} ${HELLO_LIB})