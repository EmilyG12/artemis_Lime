set(BOARD m5stack_core2/esp32/procpu)
cmake_minimum_required(VERSION 3.20.0)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(artemis-lime-trainer)

target_include_directories(app PRIVATE ../../libs)
target_sources(app PRIVATE
        ../libs/bt/bluetooth.c
        ../libs/bt/bt_scanner.c
        ../libs/bt/bt_advertiser.c
        #        ../../libs/bt/cli_observer.c
)


target_sources(app PRIVATE src/fight_ad.c)
