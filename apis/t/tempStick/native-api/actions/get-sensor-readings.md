# Get Sensor Readings with Temp Stick

Retrieves readings for a Temp Stick sensor over a selected period.

## Endpoint

- **Method:** `GET`
- **Path:** `/sensor/:sensor_id/readings`
- **Base URL:** `https://tempstickapi.com/api/v1`
- **Official documentation:** [Get Sensor Readings](https://tempstickapi.com/docs/#api-Sensors-Get_Sensor_Readings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | The end date in YYYY-MM-DD format if custom is selected |
| `offset` | query | `number` | yes | Timezone offset in seconds from UTC used to calculate the specified time period |
| `sensor_id` | path | `string` | yes | The ID of the sensor you want to get readings from |
| `setting` | query | `string` | yes | The time period you want to grab readings from |
| `start` | query | `string` | no | The start date in YYYY-MM-DD format if custom is selected |
