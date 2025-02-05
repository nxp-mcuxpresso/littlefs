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
        INCLUDES example/littlefs_shell
        BASE_PATH ${SdkRootDirPath}/middleware/littlefs
	)
    mcux_add_source(
        SOURCES example/littlefs_shell/lfs_mflash.c
                example/littlefs_shell/lfs_mflash.h
        BASE_PATH ${SdkRootDirPath}/middleware/littlefs
    )
endif()
