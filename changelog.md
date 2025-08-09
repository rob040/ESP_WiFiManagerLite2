## ESP_WiFiManagerLite2 (Light Weight Credentials / WiFiManager for ESP32/ESP8266) replaces ESP_WiFiManager_Lite

[![arduino-library-badge](https://www.ardu-badge.com/badge/ESP_WiFiManager_Lite.svg?)](https://www.ardu-badge.com/ESP_WiFiManager_Lite)
[![GitHub release](https://img.shields.io/github/release/khoih-prog/ESP_WiFiManager_Lite.svg)](https://github.com/rob040/ESP_WiFiManagerLite2/releases)
[![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/rob040/ESP_WiFiManagerLite2/blob/main/LICENSE)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](#Contributing)
[![GitHub issues](https://img.shields.io/github/issues/khoih-prog/ESP_WiFiManager_Lite.svg)](http://github.com/rob040/ESP_WiFiManagerLite2/issues)


---
---

## Table of Contents

* [Changelog](#changelog)
  * [Release v2.0.0-rc1](#release-v200-rc1)

---
---

## Changelog

### Release v2.0.0-rc1

See this as a pre version 2 of this library

1. Massive simplification to reset detector configuration
2. Using the simplified MultiResetDetector v2.0, makes the DoubleResetDetector library superfluous, hence, DRD option was removed, and MRD is now included in this library.
3. Replaced everywhere "Customs" with "Custom" (spelling error introduced in v1.2.0).
4. Flexible number of wifi credentials NUM_WIFI_CREDENTIALS; now supports 1...n configurable WiFi SSID's
5. Reviewed / changed html generation,
6. Compile warnings removed; configuration messages as warnings only at log level > 3,
7. Fix startup with erased flash: load default configuration,
8. Have storage in FS and EEPROM behave te same,
9. Resolve the getRFC952_hostname issues, renamed to setWmlHostname()
10. Do LOAD_DEFAULT_CONFIG_DATA (restore default configuration on EVERY startup) from 5 to 1 place: begin(),
11. Rename loadAndSaveDefaultConfigData() method to restoreDefaultConfiguration(),
12. Rework isWiFiConfigValid(),
13. Fix hadConfigData flag usage, and rename to present tense hasConfigData, (now it operates as a 'Cached' flag for several get functions)
14. Method setHostName now accepts a hostname argument.

BREAKING Changes:
1. Renamed "Customs" to "Custom";  This affects users with configurable **Custom HTML Headers**, including Custom Style and Custom Head Elements.
2. Renamed loadAndSaveDefaultConfigData() method to restoreDefaultConfiguration()

Known Issues:
- None yet...

### Previous Releases

All previous releases are located at https://github.com/khoih-prog/ESP_WiFiManager_Lite/
