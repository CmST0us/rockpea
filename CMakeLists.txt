cmake_minimum_required(VERSION 3.0)
project(rockpea)

set(CMAKE_C_STANDARD "99")
set(CMAKE_C_COMPILER "aarch64-linux-gnu-gcc")

add_executable(
        gpio_example
        examples/gpio_example.c
        src/gpio.c
        src/peripheral.c
)

target_include_directories(
        gpio_example
        PUBLIC
        src/
)
