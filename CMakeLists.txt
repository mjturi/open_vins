cmake_minimum_required(VERSION 3.3)

# Project name
project(open_vins)

add_subdirectory(ov_core)
add_subdirectory(ov_init)
add_subdirectory(ov_msckf)

# Optionally build the eval module, might not needed if building for a drone/robotic system
option(BUILD_OV_EVAL "Enable or disable building of ov_eval" OFF)
if (BUILD_OV_EVAL)
	add_subdirectory(ov_eval)
endif()

