# Copyright (c) OpenMMLab. All rights reserved.

project(mmdeploy_operation_cpu)

set(SRCS resize.cpp
        cvtcolor.cpp
        pad.cpp
        to_float.cpp
        hwc2chw.cpp
        normalize.cpp
        crop.cpp
        flip.cpp
        warp_affine.cpp
        crop_resize_pad.cpp)

mmdeploy_add_module(${PROJECT_NAME} "${SRCS}")

target_link_libraries(${PROJECT_NAME} PRIVATE
        mmdeploy_operation
        mmdeploy_opencv_utils)
