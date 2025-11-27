# blueprints
Blueprint collection for Home Assistant. Sonoff Zigbee Button forked and adapted for z2m from apollo1220/blueprints.

## Sonoff Zigbee Button Zigbee2MQTT
Provide the device of the button running on Zigbee2MQTT and what you want to happen on press, double press and hold.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fsflabbe%2Fblueprints%2Fblob%2Fmain%2Fsonoff_zigbee_button_z2m.yaml)

## Plant Watering Check
Provide a list of moisture sensors of plants for producing a notification when the moisture is lower than a provided moisture level for a provided list of devices at a specific hour of the day. 

Moisture Sensor List example:
```yaml
- name: Jalapeño
  sensor: sensor.jalapeno_soil_moisture
#...
- name: Habanero
  sensor: sensor.habanero_soil_moisture
```

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fsflabbe%2Fblueprints%2Fblob%2Fmain%2Fplant_watering_check.yaml)

## Low Battery Detection & Notification
Enhanced low battery detection blueprint compatible with Zigbee2MQTT 2.6.3-1 and Home Assistant Core 2025.11.3. Regularly checks all battery sensors and sends notifications when batteries are running low.

### Features
- Monitors all sensors with 'battery' device class
- Configurable battery threshold (5-100%)
- Schedule checks at specific time and day of week
- Exclude specific sensors from monitoring
- Optional area and floor information in notifications
- Handles unavailable/unknown device states
- Works with both percentage and binary battery sensors
- Fully compatible with Zigbee2MQTT devices

### Configuration Options
- **Battery warning level threshold**: Set the percentage below which batteries are considered low (default: 20%)
- **Time to test on**: Daily check time (default: 10:00:00)
- **Weekday to test on**: Run every day (0) or specific weekday (1-7 for Mon-Sun)
- **Excluded Sensors**: Battery sensors to exclude (e.g., smartphones)
- **Include area information**: Add floor/area location to notifications
- **Actions**: Define what happens when low batteries are detected (notifications, etc.)

### Usage
The `{{sensors}}` variable will contain a comma-separated list of low battery sensors with their current percentage, for example:
```
Living Room Motion Sensor [Ground Floor/Living Room] (15%), Kitchen Door Sensor (12%)
```

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fsflabbe%2Fblueprints%2Fblob%2Fmain%2Flow-battery-detection.yaml)
