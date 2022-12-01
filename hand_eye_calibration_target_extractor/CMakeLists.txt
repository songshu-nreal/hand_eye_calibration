cmake_minimum_required(VERSION 2.8.3)
project(hand_eye_calibration_target_extractor)

if(NOT ANDROID_NREAL)
    find_package(catkin_simple REQUIRED)
    catkin_simple(ALL_DEPS_REQUIRED)

    add_definitions(--std=c++11)

    cs_add_executable(target_extractor src/target_extractor.cc)

    cs_install()
    cs_export()
endif()