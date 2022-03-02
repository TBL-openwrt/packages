include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_NAME:=python-libmodbustbl
PKG_VERSION:=0.0.1
PKG_RELEASE:=1

PKG_LICENSE:=BSD-3-Clause
PKG_MAINTAINER:=Daniel Golle <daniel@makrotopia.org>

PYPI_NAME:=pylibmodbustbl
PKG_SOURCE_URL:=https://github.com/TBL-openwrt/modbus2mqtt.git
PKG_SOURCE_VERSION:=73c31df28c91f655061421546a687802a799bd1e
PKG_HASH:=skip

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-libmodbustbl
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=pylibmodbustbl
  URL:=https://github.com/TBL-openwrt/pylibmodbus.git
  DEPENDS:=+libmodbus \
     +python3-light \
     +python3-cffi
endef

define Package/python3-libmodbustbl/description
	Python Interface for libmodbus written with CFFI with added flush calls
endef

$(eval $(call Py3Package,python3-libmodbustbl))
$(eval $(call BuildPackage,python3-libmodbustbl))
