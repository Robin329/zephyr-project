# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)

set(BOARD_ROOT ${CMAKE_CURRENT_LIST_DIR})
# set(DTC_OVERLAY_FILE $(CMAKE_CURRENT_SOURCE_DIR)/boards/esp32c3_devkitm.overlay)
# set(OVERLAY_CONFIG $(CMAKE_CURRENT_SOURCE_DIR)/boards/esp32c3_devkitm.conf)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(led_ssd1306)

FILE(GLOB app_sources src/*.c)
target_sources(app PRIVATE ${app_sources})
