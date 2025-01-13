cmake_minimum_required(VERSION 3.17)
project(TryCoroutine LANGUAGES CXX)  # 项目名称和语言

set(CMAKE_CXX_STANDARD 20)  # 使用 C++20 标准
set(CMAKE_CXX_STANDARD_REQUIRED ON)  # 强制使用 C++20
set(CMAKE_CXX_EXTENSIONS OFF)  # 禁用编译器扩展

# 启用协程支持（GCC 需要）
if (CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
    add_compile_options(-fcoroutines)  # GCC 需要 -fcoroutines 标志
endif()

add_executable(main0 main0.cpp)
add_executable(main1 main1.cpp)
add_executable(main2 main2.cpp)
add_executable(main3 main3.cpp)
add_executable(main4 main4.cpp)
add_executable(main5 main5.cpp)