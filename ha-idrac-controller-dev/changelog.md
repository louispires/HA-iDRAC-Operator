## 0.1.0-dev.15 - 2026-09-22

* 🐛 **Bug Fix**: The `temperature_unit` option now actually works. When set to `F`, fan thresholds, the PID target temperature, and fan curve points are converted to Celsius before being compared against sensor readings. Previously the option was read by `run.sh` but ignored by the app, so Fahrenheit values were treated as Celsius.
* 🎨 **UI Improvement**: Temperature input labels on the Add and Edit Server pages now show the configured unit instead of always showing °C.
* 🔧 **Improvement**: The `check_interval_seconds` fallback default now matches the add-on config default of 30 seconds (was 60).

## 0.1.0-dev.14 - 2026-09-22

* 🐛 **Bug Fix**: MQTT client ID is now unique per add-on instance. Running two copies of the add-on no longer causes the broker to kick both clients in an endless connect/disconnect loop that re-published discovery messages and slowed Home Assistant down.
* 🔧 **Improvement**: Added reconnect backoff (1s to 120s) so a broker problem no longer floods the add-on log.

## 0.1.0-dev.13 - 2025-09-24

* ✨ **New Feature**: Added a "monitor-only" mode to disable fan control on a per-server basis.
* 🐛 **Bug Fix**: The addon now correctly parses power consumption from older iDRAC 6 servers using the "System Level" sensor.
* 🎨 **UI Improvement**: Added a "Fan Control" dropdown to the Add and Edit Server pages.

## 0.1.0-dev.12 - 2025-09-20

* Previous updated release.