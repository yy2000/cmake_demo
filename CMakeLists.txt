
cmake_minimum_required(VERSION 3.0)
project(demo)

#Bring the headers, such as Student.h into the project
include_directories(include)

#Can manually add the sources using the set command as follows:
#set(SOURCES src/m.cpp src/s.cpp)

#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "demo/*.C")

add_executable(demo ${SOURCES})

install(TARGETS demo DESTINATION ${PROJECT_BINARY_DIR}/bin)

