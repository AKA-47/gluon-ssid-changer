ssid-changer
============

Script to change the SSID when there is no suffic sufficient connection to the selected Gateway.

It is quite basic, it just checks the Quality of the Connection and decides if a change of the SSID is necessary.

Create a file "modules" with the following content in your site directory:</a>

GLUON_SITE_FEEDS="ssidchanger"<br>
PACKAGES_SSIDCHANGER_REPO=https://github.com/AKA-47/gluon-ssid-changer.git<br>
PACKAGES_SSIDCHANGER_COMMIT=d419ea632dc55ae371464876cef391aa4eace5f1<br>

With this done you can add the package gluon-ssid-changer to your site.mk

13.12.2015: Working on some fixes for 2015.2
