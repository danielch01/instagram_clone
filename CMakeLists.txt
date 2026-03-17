# =========================
# Build configuration:
# 1. mkdir build
# 2. cd build
# 3. cmake ..
# 4. make (compliles the file)
# 5. cd ..
# 6. ./src/main
# =========================

cmake_minimum_required(VERSION 3.10)

project(igClone)

add_executable(ig_clone
    src/main.cpp
)

