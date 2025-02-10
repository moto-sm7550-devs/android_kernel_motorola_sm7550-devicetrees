#remove useless qcom device tree in moto build
ifneq ($(CONFIG_MMI_DEVICE_DTBS),y)
dtbo-y += kalama-ese-mtp.dtbo
dtbo-y += kalama-ese-cdp.dtbo
dtbo-y += kalama-ese-qrd.dtbo

dtbo-y += kalama-v2-ese-mtp.dtbo
dtbo-y += kalama-v2-ese-cdp.dtbo
dtbo-y += kalama-v2-ese-qrd.dtbo
endif

#Moto ese dtbo
dtbo-$(CONFIG_RTWO_DTB) += kalama-ese-rtwo-evb1.dtbo

dtbo-$(CONFIG_CTWO_DTB) += kalama-ese-ctwo-evb.dtbo

dtbo-$(CONFIG_ARC_DTB) += kalama-ese-arc-evb.dtbo

always-y	:= $(dtb-y) $(dtbo-y)
subdir-y	:= $(dts-dirs)
clean-files	:= *.dtb *.dtbo
