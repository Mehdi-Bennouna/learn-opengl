    cmake_minimum_required(VERSION 3.16)
    project(app VERSION 0.1.0 DESCRIPTION "learn-opengl")

    set(CMAKE_CXX_STANDARD 20)
    set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/bin)
    set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
    set(SOURCE_FILES src/main.cpp)

    add_executable(app ${SOURCE_FILES})

    target_include_directories(app PRIVATE include)
    target_link_directories(app PRIVATE lib)

    target_link_libraries(app glfw3 GL X11 pthread glad)

    set(CMAKE_EXPORT_COMPILE_COMMANDS ON CACHE INTERNAL "") 
