cmake_minimum_required(VERSION 3.20.0)
zephyr_library()

zephyr_library_sources(
        bt_advertiser.c
        bt_scanner.c
        bluetooth.c
)