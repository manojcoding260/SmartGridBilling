cmake_minimum_required(VERSION 3.20)
project(SmartGridBilling)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Tell CLion where to find header files so you can use #include "models/"[cite: 1]
include_directories(${CMAKE_SOURCE_DIR}/include)

# Recursively find all source files in the src directory[cite: 1]
file(GLOB_RECURSE SOURCES "src/*.cpp")

# Create the executable[cite: 1]
add_executable(SmartGridBilling ${SOURCES})

# Note: To link your local MySQL 9.7.2, you will need to add the MySQL include directories and target_link_libraries here once downloaded.