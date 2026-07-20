# Disable Alerts for Device with Dotcom Monitor

Disables alerts for a device in Dotcom Monitor temporarily.

## Endpoint

- **Method:** `POST`
- **Path:** `/device/:deviceId/DisableAlert`
- **Base URL:** `https://api.dotcom-monitor.com/config_api_v1`
- **Official documentation:** [Disable Alerts for Device](https://www.dotcom-monitor.com/wiki/knowledge-base/api-disable-alerts-for-a-device/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Alert_Silence_min` | body | `number` | yes | The number of minutes to disable alerts for this device. |
| `device_id` | path | `string` | yes | The unique monitoring device ID. |
