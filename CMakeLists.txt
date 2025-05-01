cmake_minimum_required(VERSION 3.23)

message(STATUS "STM32F1xx_CMSIS_Core interface library")

if(CMAKE_SOURCE_DIR STREQUAL CMAKE_CURRENT_SOURCE_DIR)
  message(STATUS "Library loaded as to project")

  project(
    STM32F1xx_CMSIS_Core_Project
    DESCRIPTION "STM32F1xx_CMSIS_Core headers"
    LANGUAGES C ASM
  )

  set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
endif()

add_library(STM32F1xx_CMSIS_Core INTERFACE)

target_include_directories(
  STM32F1xx_CMSIS_Core
  INTERFACE
  Drivers/CMSIS/Include
  Drivers/CMSIS/Core/Include
)
