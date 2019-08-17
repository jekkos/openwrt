# Copyright (C) 2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.

include $(TOPDIR)/rules.mk

PKG_NAME:=ltq-vdsl-fw
PKG_VERSION:=6.8.6
PKG_RELEASE:=3

PKG_MAINTAINER:=Daniel Golle <daniel@makrotopia.org>

PKG_FLAGS:=nonshared

include $(INCLUDE_DIR)/package.mk

define Package/ltq-vdsl-vr9-vectoring-fw-installer
  TITLE:=VDSL2 Vectoring Firmware installer
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=@TARGET_lantiq_xrx200 +kmod-ltq-vdsl-vr9
endef

define Package/ltq-vdsl-vr9-vectoring-fw-installer/install
	$(INSTALL_DIR) $(1)/lib/firmware
	$(CP) $(PKG_BUILD_DIR)/lantiq-vrx200-b.bin $(1)/lib/firmware
endef

$(eval $(call BuildPackage,ltq-vdsl-vr9-vectoring-fw-installer))
