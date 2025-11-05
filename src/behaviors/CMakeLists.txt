# Copyright (c) 2025 The ZMK Contributors
# SPDX-License-Identifier: MIT
if(CONFIG_ZMK_BEHAVIOR_CAPS_WORD_CUSTOM AND (CONFIG_ZMK_SPLIT_ROLE_CENTRAL OR NOT CONFIG_ZMK_SPLIT))
    zephyr_library()
    zephyr_library_sources(behavior_caps_word_custom.c)
    zephyr_library_sources(${ZEPHYR_BASE}/misc/empty_file.c)
    zephyr_library_include_directories(${ZEPHYR_LVGL_MODULE_DIR})
    zephyr_library_include_directories(${ZEPHYR_BASE}/drivers)  
    zephyr_library_include_directories(${CMAKE_SOURCE_DIR}/include)
endif()