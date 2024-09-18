cmake_minimum_required(VERSION 3.10)
project(toggleLed C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)

# Add the executable target
add_executable(toggleLed src/main.c)

# Specify the path to the cross-compiled WiringPi installation
set(WIRINGPI_DIR "/home/houssem/WiringPi/wiringPi")

# Include the WiringPi headers
include_directories(${WIRINGPI_DIR})

# Link the cross-compiled WiringPi shared library
target_link_libraries(toggleLed ${WIRINGPI_DIR}/libwiringPi.so.3.10)
