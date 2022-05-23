cmake_minimum_required(VERSION 3.20)
project(FlappyBird)

find_package(SFML 2.5 REQUIRED network audio graphics window system)

set(CMAKE_CXX_STANDARD 14)

add_executable(FlappyBird main.cpp)

file(COPY ${CMAKE_CURRENT_SOURCE_DIR}/res DESTINATION ${CMAKE_CURRENT_BINARY_DIR})
include_directories(${SFML_INCLUDE_DIR})
target_link_libraries(${PROJECT_NAME} sfml-graphics sfml-audio sfml-window sfml-system)
