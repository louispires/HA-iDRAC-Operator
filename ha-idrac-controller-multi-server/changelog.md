## 0.1.0-ms.4 - 2026-09-22

* 🐛 **Bug Fix**: The `temperature_unit` option now actually works. When set to `F`, fan thresholds, the PID target temperature, and fan curve points are converted to Celsius before being compared against sensor readings. Previously the option was read by `run.sh` but ignored by the app, so Fahrenheit values were treated as Celsius.
* 🎨 **UI Improvement**: Temperature input labels on the Add and Edit Server pages now show the configured unit instead of always showing °C.
* 🔧 **Improvement**: The `check_interval_seconds` fallback default now matches the add-on config default of 30 seconds (was 60).

## 0.1.0-ms.3 - 2026-09-22

* ✨ **New Feature**: Added a "monitor-only" mode to disable fan control on a per-server basis, with a "Fan Control" dropdown on the Add and Edit Server pages.
* 🐛 **Bug Fix**: Power consumption is now parsed correctly on older iDRAC 6 servers, which report the "System Level" sensor instead of "Pwr Consumption".
* 🐛 **Bug Fix**: The "Back to Server List" link on the Edit Server page no longer resolves to a dead URL.

## 0.1.0-ms.2 - 2026-09-22

* 🐛 **Bug Fix**: MQTT client ID is now unique per add-on instance. Running two copies of the add-on no longer causes the broker to kick both clients in an endless connect/disconnect loop.
* 🔧 **Improvement**: Added MQTT reconnect backoff (1s to 120s).

## 0.1.0-ms.1

* Initial multi-server release, branched from the development variant.
