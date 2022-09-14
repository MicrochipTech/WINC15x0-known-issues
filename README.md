# WINC15x0-known-issues
More info may be available via WINC15x0 Harmony 3 release notes [here](https://github.com/Microchip-MPLAB-Harmony/wireless_apps_winc1500/blob/master/release_notes.md)

| No.		| Deliverable 	| ID | Issue / Limitation | Affected Version(s) | Fix Version(s) | Recommendation |
| ----- | ------------- | -- | ------------------ | ------------------- | -------------- | -------------- |
| 1 | MQTT example | - | Cannot connect to MQTT borker set by default in the example | ASF release 3.51 | - | In *main.h*, change **main_mqtt_broker** to *"test.mosquitto.org"*. In *main.c*, look for fucntion call **mqtt_connect_broker()** and change MQTT cient ID passed to fucntion (5th argument) to *NULL* |
| 2 | WINC1500 FIRMWARE UPDATE PROJECT | - | Failure to use the board-specific XO offset stored in efuse when calculating lookup tables during image creation/flashing.This may result in sub-optimal RF performance. | ASF release 3.51 (FW Version 19.7.7) | FW version 19.7.7 |  The release zip [WINC1500 FIRMWARE UPDATE PROJECT](https://github.com/MicrochipTech/WINC-Releases/blob/master/WINC1500/19_7_7/WINC1500_FIRMWARE_UPDATE_PROJECT.7z) is updated with script "update_pll_table.bat" which will handle the extraction of XO offset from efuse, and ensure the value is used correctly during image creation. |

