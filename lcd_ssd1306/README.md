# Zephyr_ESP32_OLED_SSD1306_I2C

## Overview

Zephyr standup using SSD1306 OLED display with I2C interface and Character Feame Buffer (CFB) library, CFB is a much lighter weight grpahics driver than LVGL for example if you dont need fancy graphics

## Requirements

1. ESP32 Devkit C
2. Zephyr OS and West installed
3. SSD1306 I2C based OLED display 128x64

## Wiring and connections

DISPLAY    ESP32
VSS  --  GND
VDD  --  3V3
SCL  --  GPIO22
SDA  --  GPIO21



## Building and Running
Initially and everytine you start a shell please run:
<br>
$>source ~/zephyrproject/zephyr/zephyr-env.sh

Build and flash as follows:
<br>
For the first build:

For esp32_devkitc_wroom board

$> west build -p -b esp32_devkitc_wroom


For subsequent builds:

$> west build


To Flash:

$> west flash


After flashing, optinally view the printk output on a terminal emnulator @ 115200, no handshaking

$> west flash ; minicom
