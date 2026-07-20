# Stop Session with Browser Use

Stops a session or running task in Browser Use.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:session_id/stop`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Stop Session](https://docs.browser-use.com/cloud/api-v3/sessions/stop-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | Browser Use session ID. |
| `strategy` | body | `list` | no | Stop strategy: task or session. Accepted values: `0`, `1`. |
