# Copyright (c) 2021 Nordic Semiconductor ASA
# SPDX-License-Identifier: Apache-2.0
#
# This CMake file is picked by the Zephyr build system because it is defined
# as the module CMake entry point (see zephyr/module.yml).

cmake_minimum_required(VERSION 3.20.0)

list(APPEND SOC_ROOT ${CMAKE_CURRENT_SOURCE_DIR}/)
list(APPEND DTS_ROOT ${CMAKE_CURRENT_SOURCE_DIR}/)
list(APPEND BOARD_ROOT ${CMAKE_CURRENT_SOURCE_DIR}/)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
# set(BOARD lpcxpresso55s36)

project(my_zephyr_app)

target_sources(app PRIVATE src/main.c)

# add_subdirectory(drivers)
