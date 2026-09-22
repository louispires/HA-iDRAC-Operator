## 0.1.0-dev.14 - 2026-09-22

* 🐛 **Bug Fix**: MQTT client ID is now unique per add-on instance. Running two copies of the add-on no longer causes the broker to kick both clients in an endless connect/disconnect loop that re-published discovery messages and slowed Home Assistant down.
* 🔧 **Improvement**: Added reconnect backoff (1s to 120s) so a broker problem no longer floods the add-on log.

## 0.1.0-dev.13 - 2025-09-24

* ✨ **New Feature**: Added a "monitor-only" mode to disable fan control on a per-server basis.
* 🐛 **Bug Fix**: The addon now correctly parses power consumption from older iDRAC 6 servers using the "System Level" sensor.
* 🎨 **UI Improvement**: Added a "Fan Control" dropdown to the Add and Edit Server pages.

## 0.1.0-dev.12 - 2025-09-20

* Previous updated release.