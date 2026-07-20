# List Monitoring Locations with Dotcom Monitor

Retrieves monitoring locations for a platform from Dotcom Monitor.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations/:platform_name`
- **Base URL:** `https://api.dotcom-monitor.com/config_api_v1`
- **Official documentation:** [List Monitoring Locations](https://www.dotcom-monitor.com/wiki/knowledge-base/monitoring-agents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform_name` | path | `string` | yes | Platform name segment from Dotcom Monitor monitoring platforms. |
