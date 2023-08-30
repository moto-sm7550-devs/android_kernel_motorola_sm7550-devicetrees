#remove useless qcom device tree in moto build
ifneq ($(CONFIG_MMI_DEVICE_DTBS),y)
ifeq ($(CONFIG_ARCH_KALAMA), y)
dtbo-y += kalama-audio.dtbo \
                 kalama-audio-cdp.dtbo \
                 kalama-audio-cdp-nfc.dtbo \
                 kalama-audio-wsa883x-cdp.dtbo \
                 kalama-audio-cdp-apq.dtbo \
                 kalama-audio-mtp.dtbo \
                 kalama-audio-mtp-nfc.dtbo \
                 kalama-audio-mtp-apq.dtbo \
                 kalama-audio-qrd.dtbo \
                 kalama-audio-atp.dtbo \
                 kalama-audio-rcm.dtbo \
                 kalama-audio-rumi.dtbo \
                 kalama-audio-hdk.dtbo \
                 kalama-sg-audio-hhg.dtbo \
                 kalama-audio-rb5-gen2.dtbo
endif
else

dtbo-$(CONFIG_ARCH_KALAMA) += kalama-audio.dtbo
dtbo-$(CONFIG_RTWO_DTB) += kalama-audio-moto-rtwo-evb1.dtbo \
                           kalama-audio-moto-rtwo-dvt1b.dtbo

dtbo-$(CONFIG_OBERON_DTB) += kalama-audio-moto-oberon-evb.dtbo

dtbo-$(CONFIG_CTWO_DTB) += kalama-audio-moto-ctwo-evb.dtbo

dtbo-$(CONFIG_ARC_DTB) += kalama-audio-moto-arc-evb.dtbo

dtbo-$(CONFIG_BELMONT_DTB) += kalama-audio-moto-belmont-evb.dtbo

endif  #($(CONFIG_MMI_DEVICE_DTBS),y)

ifeq ($(CONFIG_ARCH_SA8155), y)
dtbo-y +=  sa8155-audio.dtbo
endif

ifeq ($(CONFIG_ARCH_KHAJE), y)
dtbo-y += khaje-audio.dtbo \
		khaje-audio-idp.dtbo \
		khaje-audio-qrd.dtbo \
		khaje-audio-qrd-hvdcp3p5.dtbo \
		khaje-audio-idp-nopmi.dtbo \
                khajeg-audio-idp.dtbo \
                khajeg-audio-idp-90hz.dtbo \
		khaje-nowcd.dtbo
endif

ifeq ($(CONFIG_ARCH_CROW), y)
#remove useless qcom device tree in moto build
ifneq ($(CONFIG_MMI_DEVICE_DTBS),y)
dtbo-y += crow-audio.dtbo \
                 crow-audio-idp.dtbo \
                 crow-audio-idp-wcd9395-aatc.dtbo \
                 crow-audio-idp-wcd9395-dmic.dtbo \
                 crow-audio-idp-wcd9395-wcd-dmic.dtbo \
                 crow-audio-qrd.dtbo \
                 crow-audio-atp.dtbo

else
dtbo-$(CONFIG_ARCH_CROW) += crow-audio.dtbo
dtbo-$(CONFIG_EQE_DTB) += crow-audio-moto-eqe-evb.dtbo
dtbo-$(CONFIG_EQE_DTB) += crow-audio-moto-eqe-evt.dtbo
endif  #($(CONFIG_MMI_DEVICE_DTBS),y)
endif

 always-y    := $(dtb-y) $(dtbo-y)
 subdir-y    := $(dts-dirs)
 clean-files    := *.dtb *.dtbo
