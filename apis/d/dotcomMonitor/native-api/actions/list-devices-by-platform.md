# List Devices by Platform with Dotcom Monitor

Retrieves devices for a monitoring platform from Dotcom Monitor.

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/:platform_name`
- **Base URL:** `https://api.dotcom-monitor.com/config_api_v1`
- **Official documentation:** [List Devices by Platform](https://www.dotcom-monitor.com/wiki/knowledge-base/get-device-list-by-platform/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform_name` | path | `string` | yes | The monitoring platform name whose devices should be listed. |
