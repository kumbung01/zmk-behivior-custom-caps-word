# Copyright (c) 2025 The ZMK Contributors
# SPDX-License-Identifier: MIT

zephyr_library()

if(CONFIG_ZMK_SPLIT_ROLE_CENTRAL OR NOT CONFIG_ZMK_SPLIT)
    set(ZMK_APP_DIR ${CMAKE_CURRENT_SOURCE_DIR}/../zmk/app)

    target_sources(app PRIVATE
        ${ZMK_APP_DIR}/src/hid.c
        ${ZMK_APP_DIR}/src/events/keycode_state_changed.c
    )
endif()