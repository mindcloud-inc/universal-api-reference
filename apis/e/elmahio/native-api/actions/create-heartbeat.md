# Create Heartbeat with elmah.io

Creates a new heartbeat in elmah.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/heartbeats/:logId/:id`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Create Heartbeat](https://api.elmah.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | path | `string` | yes | The ID of the log containing the heartbeat check. |
| `id` | path | `string` | yes | The ID of the heartbeat check. |
| `result` | body | `string` | no | The result of this heartbeat. |
| `reason` | body | `string` | no | Why the heartbeat is degraded or unhealthy. |
| `application` | body | `string` | no | Optional application name to associate with the heartbeat. |
| `version` | body | `string` | no | Optional application version to associate with the heartbeat. |
| `took` | body | `number` | no | How many milliseconds the task took to execute. |
| `checks[]` | body | `array<object>` | no | A list of individual checks included in the heartbeat. |
| `name` | body | `string` | no | The name of the individual check. |
| `took` | body | `number` | no | How many milliseconds the individual check took. |
| `result` | body | `string` | no | The result of the individual check. |
| `reason` | body | `string` | no | Why the individual check is degraded or unhealthy. |
