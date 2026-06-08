cmake_minimum_required(VERSION 3.20)
project(OpenGLTest)

set(CMAKE_CXX_STANDARD 20)

find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(OpenGLTest
    src/main.cpp
    external/glad/src/gl.c
)

target_include_directories(OpenGLTest PRIVATE
    external/glad/include
)

target_link_libraries(OpenGLTest PRIVATE
    glfw
    OpenGL::GL
)
