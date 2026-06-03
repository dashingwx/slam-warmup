cmake_minimum_required(VERSION 3.16)
project(Week2_Nonlinear_Optimization LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 查找 Eigen3
find_package(Eigen3 REQUIRED)

# 生成 compile_commands.json（给 clangd / IDE 用）
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# eigenMatrix
add_executable(eigenMatrix eigenMatrix.cpp)
target_link_libraries(eigenMatrix Eigen3::Eigen)

# useGeometry
add_executable(useGeometry useGeometry.cpp)
target_link_libraries(useGeometry Eigen3::Eigen)
