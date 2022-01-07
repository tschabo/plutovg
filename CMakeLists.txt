cmake_minimum_required(VERSION 3.3)

set(CMAKE_C_STANDARD 11)

project(plutovg C)

add_library(plutovg)

add_subdirectory(include)
add_subdirectory(source)
add_subdirectory(3rdparty/stb)
add_subdirectory(3rdparty/software)
option(ENABLE_BUILD_EXAMPLE "Turn on to enable tests" OFF)
if (ENABLE_TEST)
    add_subdirectory(example)
endif()

install(TARGETS plutovg DESTINATION "."
        PUBLIC_HEADER DESTINATION include
        RUNTIME DESTINATION bin
        ARCHIVE DESTINATION lib
        LIBRARY DESTINATION lib
        )