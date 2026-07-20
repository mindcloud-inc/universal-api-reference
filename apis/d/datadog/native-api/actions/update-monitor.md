# Update Monitor with Datadog

Updates an existing monitor in Datadog.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/monitor/:monitor_id`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Update Monitor](https://docs.datadoghq.com/api/latest/monitors/#edit-a-monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Updated notification message. |
| `monitor_id` | path | `number` | yes | The ID of the monitor to edit. |
| `name` | body | `string` | no | Updated monitor name. |
| `options` | body | `object` | no | Updated monitor options object. |
| `priority` | body | `number` | no | Updated alert severity from 1 (high) to 5 (low). |
| `query` | body | `string` | no | Updated monitor query expression. |
| `restricted_roles[]` | body | `array<string>` | no | Updated role IDs allowed to edit the monitor. |
| `tags[]` | body | `array<string>` | no | Updated monitor tags. |
| `type` | body | `string` | no | Updated Datadog monitor type. |
