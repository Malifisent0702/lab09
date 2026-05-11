cmake_minimum_required(VERSION 3.4)
project(solver)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(solver equation.cpp)

target_link_libraries(solver
    ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/build/libformatter_ex.a
    ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib/build/libformatter.a
    ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib/build/libsolver_lib.a
)

target_include_directories(solver PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib
    ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib
    ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib
)
