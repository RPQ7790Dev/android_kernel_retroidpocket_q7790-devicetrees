# SPDX-License-Identifier: GPL-2.0

add-overlays = $(foreach o,$1,$(foreach b,$2,$(eval $(basename $b)-$(basename $o)-dtbs = $b $o) $(basename $b)-$(basename $o).dtb))

KERA_BASE_DTB += ../qcom/kerap-iot.dtb
KERA_BOARDS += kerap-iot-retroid-pocket-duo-overlay.dtbo

kera-dtb-$(CONFIG_ARCH_KERA) += $(KERA_BOARDS) $(KERA_BASE_DTB)
kera-overlays-dtb-$(CONFIG_ARCH_KERA) += $(KERA_BOARDS) $(KERA_BASE_DTB)
dtb-y += $(kera-dtb-y)

always-y := $(dtb-y)
subdir-y := $(dts-dirs)
subdir-y += audio ../qcom/bt ../qcom/data display ../qcom/dsp ../qcom/eva ../qcom/graphics ../qcom/mm ../qcom/mmrm ../qcom/synx ../qcom/video ../qcom/wlan
clean-files := *.dtb *.dtbo
