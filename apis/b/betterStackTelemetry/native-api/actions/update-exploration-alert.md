# Update Exploration Alert with Better Stack Telemetry

Updates an existing exploration alert in Better Stack Telemetry.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/explorations/:exploration_id/alerts/:id`
- **Base URL:** `https://telemetry.betterstack.com`
- **Official documentation:** [Update Exploration Alert](https://betterstack.com/docs/logs/api/alerts/update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exploration_id` | path | `string` | yes | The ID of the exploration that owns the alert. |
| `id` | path | `string` | yes | The ID of the alert to update. |
| `name` | body | `string` | no | Updated alert name. |
| `value` | body | `number` | no | Updated numeric value for the alert condition. |
| `string_value` | body | `string` | no | Updated exact string match value. |
| `anomaly_sensitivity` | body | `number` | no | Updated anomaly sensitivity. |
| `confirmation_period` | body | `number` | no | Updated confirmation period in seconds. |
| `paused` | body | `boolean` | no | Updated paused state. |
| `escalation_target` | body | `object` | no | Updated notification target object. |
| `metadata` | body | `object` | no | Updated custom metadata object. |
