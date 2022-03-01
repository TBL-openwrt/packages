include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_NAME:=python-libmodbus
PKG_VERSION:=0.6.0
PKG_RELEASE:=3

PKG_LICENSE:=BSD-3-Clause
PKG_MAINTAINER:=Daniel Golle <daniel@makrotopia.org>

PYPI_NAME:=pylibmodbus
PKG_HASH:=skip

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-libmodbus
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=pylibmodbus
  URL:=https://github.com/TBL-openwrt/pylibmodbus.git
  DEPENDS:=+libmodbus \
     +python3-light \
     +python3-cffi
endef

define Package/python3-libmodbus/description
	Python Interface for libmodbus written with CFFI.
endef

$(eval $(call Py3Package,python3-libmodbus))
$(eval $(call BuildPackage,python3-libmodbus))
