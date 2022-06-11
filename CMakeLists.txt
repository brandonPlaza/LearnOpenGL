cmake_minimum_required(VERSION 3.0.0)
project(LearningOpenGL VERSION 0.1.0)

include(CTest)
enable_testing()
include_directories(lib/glfw)
include_directories(lib/glfw/deps)
include_directories(lib/glfw/include)
add_executable(LearningOpenGL main.cpp)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(LearningOpenGL PRIVATE glfw)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
