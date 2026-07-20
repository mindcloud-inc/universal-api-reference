# List Tasks by Device with Dotcom Monitor

Retrieves tasks for a device from Dotcom Monitor.

## Endpoint

- **Method:** `GET`
- **Path:** `/device/:deviceId/tasks`
- **Base URL:** `https://api.dotcom-monitor.com/config_api_v1`
- **Official documentation:** [List Tasks by Device](https://www.dotcom-monitor.com/wiki/knowledge-base/get-task-list-by-device/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_id` | path | `string` | yes | The unique monitoring device ID. |
