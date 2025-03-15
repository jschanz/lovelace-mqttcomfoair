# Homeassistant Lovelace MQTT Comfoair card

This is a modified Lovelace Comfoair card to work with the ComfoAir Service https://github.com/adorobis/hacomfoairmqtt with MQTT Autodiscovery to visualize your data!

![Image](https://raw.githubusercontent.com/TimWeyand/lovelace-comfoair/master/result.png)

## Installation

* Get the hacomfoairmqtt Service running
* Clone this repo into your `www` folder inside your configuration. So it will be: `config_folder/www/lovelace-mqttcomfoair`. 
* Edit your lovelace-ui.yaml or use the flat configuration mode in lovelace and add to the top:

![Image](https://raw.githubusercontent.com/jschanz/lovelace-mqttcomfoair/refs/heads/master/dashboard_configuration1.png)
![Image](https://raw.githubusercontent.com/jschanz/lovelace-mqttcomfoair/refs/heads/master/dashboard_configuration2.png)

```yaml
resources:
  - type: module
    url: /local/lovelace-mqttcomfoair/comfoair-card.js
```

## Configuration

* Go to your Lovelace Dashboard
* Add a "MQTT Comfoair Card" via UI
* Check the Entity Selection

![Image](https://raw.githubusercontent.com/jschanz/lovelace-mqttcomfoair/refs/heads/master/comfoair_configuration.png)
![Image](https://raw.githubusercontent.com/jschanz/lovelace-mqttcomfoair/refs/heads/master/comfoair_configuration2.png)
![Image](https://raw.githubusercontent.com/jschanz/lovelace-mqttcomfoair/refs/heads/master/comfoair_configuration3.png)

```yaml
type: custom:mqttcomfoair-card
entity: climate.ca350_climate
tempSensor1: sensor.ca350_outside_temperature
tempSensor2: sensor.ca350_exhaust_temperature
tempSensor3: sensor.ca350_return_temperature
tempSensor4: sensor.ca350_supply_temperature
filterstatus: binary_sensor.ca350_filter_status
bypass_valve: binary_sensor.ca350_bypass_valve
summer_mode: binary_sensor.ca350_summer_mode
fan_speed_supply: sensor.ca350_supply_fan_speed
fan_speed_exhaust: sensor.ca350_exhaust_fan_speed
return_air_level: sensor.ca350_return_air_level
supply_air_level: sensor.ca350_supply_air_level
```

## Controlling the Comfoair

* Click on the Fan Speed Icon

## ToDO

* [ ] Highlight the current Fan Speed Icon
* [ ] Control the Temperature
