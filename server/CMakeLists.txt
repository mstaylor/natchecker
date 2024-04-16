cmake_minimum_required(VERSION 2.8)


# Specify the C standard
set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED True)

# Add an executable with the above sources
add_executable(natserver natserver.c)
