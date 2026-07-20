# Create Monitor with Datadog

Creates a new monitor in Datadog.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/monitor`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Create Monitor](https://docs.datadoghq.com/api/latest/monitors/#create-a-monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Notification message for the monitor. |
| `name` | body | `string` | no | Human-readable monitor name. |
| `options` | body | `object` | no | Monitor options object as documented by Datadog. |
| `priority` | body | `number` | no | Alert severity from 1 (high) to 5 (low). |
| `query` | body | `string` | yes | Monitor query expression. |
| `restricted_roles[]` | body | `array<string>` | no | Role IDs allowed to edit the monitor. |
| `tags[]` | body | `array<string>` | no | Tags associated with the monitor. |
| `type` | body | `string` | no | Datadog monitor type. |
