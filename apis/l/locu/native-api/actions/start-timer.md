# Start Timer with Locu

Starts a new session timer in Locu.

## Endpoint

- **Method:** `POST`
- **Path:** `/timer/start`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Start Timer](https://locu.app/api/docs#tag/timer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `number` | yes | Timer duration in seconds. Must be a positive integer. |
| `taskId` | body | `string` | no | Optional task ID to start working on. |
