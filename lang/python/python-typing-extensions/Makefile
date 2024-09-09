#
# Copyright (C) 2021 CZ.NIC, z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-typing-extensions
PKG_VERSION:=4.9.0
PKG_RELEASE:=1

PYPI_NAME:=typing-extensions
PYPI_SOURCE_NAME:=typing_extensions
PKG_HASH:=23478f88c37f27d76ac8aee6c905017a143b0b1b886c3c9f66bc2fd94f9f5783

PKG_MAINTAINER:=Jan Pavlinec <jan.pavlinec1@gmail.com>
PKG_LICENSE:=PSF-2.0
PKG_LICENSE_FILES:=LICENSE

HOST_BUILD_DEPENDS:=python3/host python-build/host python-installer/host python-wheel/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include ../python3-package.mk
include ../python3-host-build.mk

define Package/python3-typing-extensions
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Module with type hints for Python
  URL:=https://github.com/python/typing_extensions
  DEPENDS:= \
	+python3-light
endef

define Package/python3-typing-extensions/description
  Backported and Experimental Type Hints for Python.
endef

$(eval $(call Py3Package,python3-typing-extensions))
$(eval $(call BuildPackage,python3-typing-extensions))
$(eval $(call BuildPackage,python3-typing-extensions-src))
$(eval $(call HostBuild))
