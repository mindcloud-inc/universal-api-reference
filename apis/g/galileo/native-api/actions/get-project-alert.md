# Get Project Alert with Galileo

Retrieves an alert from a Galileo project by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/projects/:project_id/alerts/:monitor_alert_config_id`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Get Project Alert](https://docs.galileo.ai/api-reference/log-stream-alerts/get-alert-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `monitor_alert_config_id` | path | `string` | yes | Galileo monitor alert configuration UUID. |
| `project_id` | path | `string` | yes | Galileo project UUID. |
