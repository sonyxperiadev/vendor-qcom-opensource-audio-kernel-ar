ifeq ($(AUDIO_ROOT),)
AUDIO_ROOT := $(srctree)/techpack/audio
endif

ifeq ($(CONFIG_ARCH_WAIPIO), y)
include $(AUDIO_ROOT)/config/waipioauto.conf
LINUXINCLUDE += -include $(AUDIO_ROOT)/config/waipioautoconf.h
endif

ifeq ($(CONFIG_ARCH_KALAMA), y)
include $(AUDIO_ROOT)/config/kalamaauto.conf
LINUXINCLUDE += -include $(AUDIO_ROOT)/config/kalamaautoconf.h
endif

ifeq ($(CONFIG_ARCH_PARROT), y)
include $(AUDIO_ROOT)/config/parrotauto.conf
LINUXINCLUDE += -include $(AUDIO_ROOT)/config/parrotautoconf.h
endif

LINUXINCLUDE += \
		-I$(AUDIO_ROOT)/include/uapi \
		-I$(AUDIO_ROOT)/include/uapi/audio \
		-I$(AUDIO_ROOT)/include/asoc \
		-I$(AUDIO_ROOT)/include
USERINCLUDE += -I$(AUDIO_ROOT)/include/uapi/audio

obj-y += asoc/
obj-y += dsp/
obj-y += ipc/
obj-y += soc/
