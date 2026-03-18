# =========================
# Build configuration:
# 1. mkdir build
# 2. cd build
# 3. cmake ..
# 4. make (compliles the file)
# 5. cd ..
# 6. ./src/main
# =========================

cmake_minimum_required(VERSION 3.15)

project(ig_clone LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_executable(ig_clone
    src/main.cpp
)

target_include_directories(ig_clone
    PRIVATE
        ${CMAKE_SOURCE_DIR}/third_party/Crow/include
        ${CMAKE_SOURCE_DIR}/include
        /opt/homebrew/include   # 👈 Apple Silicon (M1/M2/M3)
)

find_package(Threads REQUIRED)

target_link_libraries(ig_clone
    PRIVATE
        Threads::Threads
)