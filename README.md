# blueprints

Blueprint collection for Home Assistant. Sonoff Zigbee Button forked and adapted for z2m from apollo1220/blueprints.

## Sonoff Zigbee Button Zigbee2MQTT
Provide the device of the button running on Zigbee2MQTT and what you want to happen on press, double press and hold.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fsflabbe%2Fblueprints%2Fblob%2Fmain%2Fsonoff_zigbee_button_z2m.yaml)

## Plant Watering Check
Provide a list of moisture sensors of plants for producing a notification when the moisture is lower than a provided moisture level for a provided list of devices at a specific hour of the day. 

Moisture Sensor List example:

```
- name: Jalapeño
  sensor: sensor.jalapeno_soil_moisture
#...
- name: Habanero
  sensor: sensor.habanero_soil_moisture
```

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fsflabbe%2Fblueprints%2Fblob%2Fmain%2Fplant_watering_check.yaml)
