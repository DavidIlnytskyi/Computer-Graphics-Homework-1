cmake_minimum_required(VERSION 3.31)
project(Homework_1)

set(CMAKE_CXX_STANDARD 20)

find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

# Create GLAD library
add_library(glad STATIC glad/glad.c)
target_include_directories(glad PUBLIC glad)

add_executable(Homework_1 main.cpp)

target_include_directories(Homework_1 PRIVATE .)

target_link_libraries(Homework_1 PRIVATE glfw OpenGL::GL glad)