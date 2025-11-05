# Copyright (c) 2025 The ZMK Contributors
# SPDX-License-Identifier: MIT

zephyr_library()

zephyr_library_sources( behavior_caps_word_custom.c )
zephyr_include_directories(${APPLICATION_SOURCE_DIR}/include)
zephyr_library_include_directories(.)
target_include_directories(app PRIVATE ${CMAKE_SOURCE_DIR}/zmk/app/include)