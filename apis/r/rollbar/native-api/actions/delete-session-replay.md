# Delete Session Replay with Rollbar

Deletes an existing session replay from Rollbar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/environment/:environment/session/:sessionId/replay/:replayId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Delete Session Replay](https://docs.rollbar.com/reference/delete-a-replay)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environment` | path | `string` | yes | Replay environment slug |
| `replayId` | path | `string` | yes | Replay identifier |
| `sessionId` | path | `string` | yes | Replay session identifier |
