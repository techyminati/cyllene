#
# Copyright (C) 2018 MediaTek Inc.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 2 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#

ifeq ($(CONFIG_MACH_MT6781),y)
	PDIR = mt6781
else
	PDIR = $(MTK_PLATFORM)
endif

THERMAL_CHIP_DRIVER_DIR := $(srctree)/drivers/misc/mediatek/thermal/$(PDIR)
ccflags-y  += -I$(THERMAL_CHIP_DRIVER_DIR)/inc
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/base/power/$(PDIR)
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/gpu/hal/
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/thermal/fakeHeader/
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/sspm/v1
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/sspm
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/sspm/$(PDIR)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/sspm/v2
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/base/power/include/spm/
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/base/power/eem_v2/mt3967/inc/
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/pmic/include/
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/thermal/common/inc/
ccflags-y  += -I$(srctree)/include/dt-bindings/
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/base/power/include/gpufreq_v1/
ccflags-y  += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/$(PDIR)/include/

obj-$(CONFIG_THERMAL) += mtk_lvts_tc.o
#obj-$(CONFIG_THERMAL) += mtk_tc.o
obj-$(CONFIG_THERMAL) += mtk_tc_wrapper.o
obj-$(CONFIG_THERMAL) += mtk_thermal_ipi.o
obj-$(CONFIG_THERMAL) += mtk_pmic_efuse.o
obj-$(CONFIG_THERMAL) += mtk_ts_6366vcore.o
obj-$(CONFIG_THERMAL) += mtk_ts_6366vproc.o
obj-$(CONFIG_THERMAL) += mtk_ts_6366vgpu.o
obj-$(CONFIG_THERMAL) += mtk_ts_6366tsx.o
obj-$(CONFIG_THERMAL) += mtk_ts_6366dcxo.o
#obj-$(CONFIG_THERMAL) += mtk_ti_6315.o
