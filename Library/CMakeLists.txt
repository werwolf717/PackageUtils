cmake_minimum_required(VERSION 3.0) 

#Settings
set(PROJECT_NAME PackageUtilitiesLib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../lib)

set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
set(INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)

#assembly
add_library(${PROJECT_NAME} SHARED ${SRC_DIR}/PackageUtilities.cpp)

#install
install(TARGETS ${PROJECT_NAME} DESTINATION /usr/lib)
install(FILES ${INCLUDE_DIR}/PackageUtilities.h DESTINATION include)