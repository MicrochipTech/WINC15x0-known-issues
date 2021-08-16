# WINC15x0-known-issues
More info may be available via WINC15x0 Harmony 3 release notes [here](https://github.com/Microchip-MPLAB-Harmony/wireless_apps_winc1500/blob/master/release_notes.md)

| No.		| Deliverable 	| ID | Issue / Limitation | Affected Version(s) | Fix Version(s) | Recommendation |
| ----- | ------------- | -- | ------------------ | ------------------- | -------------- | -------------- |
| 1 | MQTT example | - | Cannot connect to MQTT borker set by default in the example | ASF release 3.51 | - | In *main.h*, change **main_mqtt_broker** to *"test.mosquitto.org"*. In *main.c*, look for fucntion call **mqtt_connect_broker()** and change MQTT cient ID passed to fucntion (5th argument) to *NULL* |

