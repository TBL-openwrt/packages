#
# Copyright (C) 2020 sramrajkar
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk
PKG_NAME:=modbus_tk
PKG_VERSION:=1.1.2
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://pypi.python.org/packages/source/m/modbus_tk
PKG_SOURCE_VERSION:=893514bbd8c92118d20a19979e0239e7cb2a63f8f1795a0271e57def09d11770
PKG_HASH:=skip

include $(INCLUDE_DIR)/package.mk
$(call include_mk, python-package.mk)

define Package/python-modbustk
  SECTION:=language-python
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=python-modbustk
  URL:=https://github.com/ljean/modbus-tk.git
  DEPENDS:=+python3 +python3-pyserial
  MAINTAINER:=Galen Collins
endef

define Package/python-modbustk/description
MODBUS polling module with some HMI support
endef

define Build/Compile
	$(call Build/Compile/PyMod,,install --prefix=/usr --root=$(PKG_INSTALL_DIR))
endef

define Package/python-modbustk/install
	$(INSTALL_DIR) $(1)$(PYTHON_PKG_DIR)
	$(CP) \
		$(PKG_INSTALL_DIR)$(PYTHON_PKG_DIR)/* \
		$(1)$(PYTHON_PKG_DIR)
endef

$(eval $(call BuildPackage,python-modbustk))