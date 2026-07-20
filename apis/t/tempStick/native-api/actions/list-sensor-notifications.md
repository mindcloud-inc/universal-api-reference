# List Sensor Notifications with Temp Stick

Retrieves the last seven days of notifications for a Temp Stick sensor.

## Endpoint

- **Method:** `GET`
- **Path:** `/sensor/notifications/:sensorId`
- **Base URL:** `https://tempstickapi.com/api/v1`
- **Official documentation:** [List Sensor Notifications](https://tempstickapi.com/docs/#api-Alerts-Get_Sensor_Notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items_per_page` | query | `number` | yes | Maximum 100 items per page |
| `page` | query | `number` | yes | Page number |
| `sensorId` | path | `string` | yes | Sensor ID |
