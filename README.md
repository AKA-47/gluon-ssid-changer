ssid-changer - 2015.2 Fixed
============

Script to change the SSID when there is no suffic sufficient connection to the selected Gateway.

It is quite basic, it just checks the Quality of the Connection and decides if a change of the SSID is necessary.

Create a file "modules" with the following content in your site directory:</a>

# Modules

GLUON_SITE_FEEDS="ssidchanger"<br>
PACKAGES_SSIDCHANGER_REPO=https://github.com/AKA-47/gluon-ssid-changer.git<br>
PACKAGES_SSIDCHANGER_COMMIT=d419ea632dc55ae371464876cef391aa4eace5f1<br>

With this done you can add the package gluon-ssid-changer to your site.mk

# site.mk

GLUON_SITE_PACKAGES := \
......
	      gluon-ssid-changer \
......

DEFAULT_GLUON_RELEASE := 15.12-v2015.2-exp-AKA47-$(shell date '+%Y%m%d')

GLUON_RELEASE ?= $(DEFAULT_GLUON_RELEASE)

GLUON_PRIORITY ?= 0
GLUON_BRANCH ?= experimental
export GLUON_BRANCH

GLUON_TARGET ?= ar71xx-generic
export GLUON_TARGET

GLUON_LANGS ?= de

