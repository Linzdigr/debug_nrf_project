# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(quantum)

# zephyr_include_directories(${CMAKE_CURRENT_SOURCE_DIR})
# zephyr_library_add_dependencies(offsets_h)
zephyr_syscall_include_directories(include)

zephyr_include_directories(include)

add_subdirectory(drivers/display/ssd1333)
list(APPEND ZEPHYR_EXTRA_MODULES ${CMAKE_CURRENT_SOURCE_DIR}/drivers/display/ssd1333)
target_sources(app PRIVATE src/main.c)

# list(APPEND ZEPHYR_EXTRA_MODULES ${CMAKE_CURRENT_SOURCE_DIR}/drivers/display/ssd1333)

target_sources(app PRIVATE
# source files...
)
