# List Monitoring Frequencies with Dotcom Monitor

Retrieves monitoring frequencies for a platform from Dotcom Monitor.

## Endpoint

- **Method:** `GET`
- **Path:** `/frequencies/:platform_name`
- **Base URL:** `https://api.dotcom-monitor.com/config_api_v1`
- **Official documentation:** [List Monitoring Frequencies](https://www.dotcom-monitor.com/wiki/knowledge-base/frequencies-list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform_name` | path | `string` | yes | Platform name segment from Dotcom Monitor monitoring platforms. |
