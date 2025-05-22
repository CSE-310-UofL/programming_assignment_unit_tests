cmake_minimum_required(VERSION 3.10)
project(RationalProject)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Include header files
include_directories(include)

# Main executable
add_executable(RationalProject
    main.cpp
    src/Rational.cpp
)

# Enable unit testing
enable_testing()
add_subdirectory(tests)
