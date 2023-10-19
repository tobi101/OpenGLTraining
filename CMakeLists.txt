cmake_minimum_required(VERSION 3.5.0)
project(OpenGLTraining VERSION 0.1.0 LANGUAGES C CXX)

set(glfw3_DIR ${PROJECT_SOURCE_DIR}/vendor/GLFW/lib/cmake/glfw3)

find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)

add_subdirectory(vendor/glad/)
add_executable(OpenGLTraining main.cpp)

target_link_libraries(OpenGLTraining glfw)
target_link_libraries(OpenGLTraining OpenGL::GL)
target_link_libraries(OpenGLTraining glad)
