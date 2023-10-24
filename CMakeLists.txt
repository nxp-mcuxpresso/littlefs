# Copyright 2024-2025 NXP
#
# SPDX-License-Identifier: BSD-3-Clause
if (CONFIG_MCUX_COMPONENT_middleware.littlefs)
    mcux_add_include(
        INCLUDES .
    )

    mcux_add_source(
        SOURCES lfs.c
                lfs.h
                lfs_util.c
                lfs_util.h
    )
endif()

if (CONFIG_MCUX_COMPONENT_middleware.littlefs_mflash)
    mcux_add_include(
        INCLUDES mflash
    )

    mcux_add_source(
        SOURCES mflash/lfs_mflash.c
                mflash/lfs_mflash.h
    )
endif()
