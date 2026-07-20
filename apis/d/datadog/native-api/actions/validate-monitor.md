# Validate Monitor with Datadog

Validates a monitor configuration in Datadog.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/monitor/validate`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [Validate Monitor](https://docs.datadoghq.com/api/latest/monitors/#validate-a-monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | no | Notification message to validate. |
| `name` | body | `string` | no | Human-readable monitor name to validate. |
| `options` | body | `object` | no | Monitor options object to validate. |
| `priority` | body | `number` | no | Alert severity from 1 (high) to 5 (low). |
| `query` | body | `string` | yes | Monitor query expression to validate. |
| `restricted_roles[]` | body | `array<string>` | no | Role IDs allowed to edit the monitor. |
| `tags[]` | body | `array<string>` | no | Tags associated with the monitor. |
| `type` | body | `string` | no | Datadog monitor type. |
