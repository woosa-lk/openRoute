include $(TOPDIR)/rules.mk

PKG_NAME:=app-infrared
PKG_RELEASE:=1.0
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/app-infrared
	SECTION:=utils
	CATEGORY:=Utilities
	TITLE:=app-infrared --prints a snarky message
endef

define Package/app-infrared/description
	If you cat't figure out what this program does, you're probably
	brain-dead and need immediate attention.
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) ./src/* $(PKG_BUILD_DIR)/
endef

define Build/Configure
endef

define Package/app-infrared/install
	$(INSTALL_DIR) $(1)/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/app-infrared $(1)/bin
endef

$(eval $(call BuildPackage,app-infrared))

