# Get Session Replay with Rollbar

Retrieves a session replay from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/environment/:environment/session/:sessionId/replay/:replayId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get Session Replay](https://docs.rollbar.com/reference/get-a-replay)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment` | path | `string` | yes | Replay environment slug |
| `replayId` | path | `string` | yes | Replay identifier |
| `sessionId` | path | `string` | yes | Replay session identifier |
