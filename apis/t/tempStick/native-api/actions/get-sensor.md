# Get Sensor with Temp Stick

Retrieves settings for a specific Temp Stick sensor.

## Endpoint

- **Method:** `GET`
- **Path:** `/sensor/:sensor_id`
- **Base URL:** `https://tempstickapi.com/api/v1`
- **Official documentation:** [Get Sensor](https://tempstickapi.com/docs/#api-Sensors-Get_Sensor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sensor_id` | path | `string` | yes | The ID of the sensor you want to get readings from |
