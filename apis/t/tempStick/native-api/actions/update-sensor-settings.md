# Update Sensor Settings with Temp Stick

Updates settings for an existing Temp Stick sensor.

## Endpoint

- **Method:** `POST`
- **Path:** `/sensor/:sensor_id`
- **Base URL:** `https://tempstickapi.com/api/v1`
- **Official documentation:** [Update Sensor Settings](https://tempstickapi.com/docs/#api-Sensors-Update_Sensor_Settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sensor_id` | path | `string` | yes | Sensor ID |
| `sensor_name` | body | `string` | yes | The display name for the sensor. |
| `send_interval` | body | `number` | yes | How often the sensor reports readings, in seconds. |
| `use_alert_interval` | body | `number` | yes | Whether alert interval throttling is enabled. |
| `alert_interval` | body | `number` | yes | Minimum time between alert notifications, in minutes. |
| `alert_temp_below` | body | `number` | no | Trigger an alert when temperature falls below this threshold. |
| `alert_temp_above` | body | `number` | no | Trigger an alert when temperature rises above this threshold. |
| `alert_humidity_below` | body | `number` | no | Trigger an alert when humidity falls below this threshold. |
| `alert_humidity_above` | body | `number` | no | Trigger an alert when humidity rises above this threshold. |
| `connection_sensitivity` | body | `number` | yes | Connection sensitivity setting for the sensor. |
| `use_offset` | body | `number` | yes | Whether temperature and humidity offsets are enabled. |
| `temp_offset` | body | `number` | yes | Temperature offset applied to readings. |
| `humidity_offset` | body | `number` | yes | Humidity offset applied to readings. |
