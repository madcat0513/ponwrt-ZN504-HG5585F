include $(TOPDIR)/rules.mk

PKG_NAME:=airoha-en7581-mt7916-npu-firmware
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/airoha-en7581-mt7916-npu-firmware
  SECTION:=firmware
  CATEGORY:=Firmware
  TITLE:=Airoha EN7581 MT7916 NPU firmware
  DEPENDS:=@TARGET_airoha_an7581
endef

define Package/airoha-en7581-mt7916-npu-firmware/description
  Vendor 98K Airoha EN7581 NPU RV32 firmware (npu_rv32.bin + npu_data.bin)
  for MT7916 WiFi RX hardware offload.
endef

define Build/Compile
endef

define Package/airoha-en7581-mt7916-npu-firmware/install
	$(INSTALL_DIR) $(1)/lib/firmware/airoha
	$(INSTALL_DATA) ./files/en7581_MT7916_npu_rv32.bin \
		$(1)/lib/firmware/airoha/en7581_MT7916_npu_rv32.bin
	$(INSTALL_DATA) ./files/en7581_MT7916_npu_data.bin \
		$(1)/lib/firmware/airoha/en7581_MT7916_npu_data.bin
endef

$(eval $(call BuildPackage,airoha-en7581-mt7916-npu-firmware))
