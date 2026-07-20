# Get Game Payload with Scoreboard Buzz

Retrieves a game payload from Scoreboard Buzz.

## Endpoint

- **Method:** `GET`
- **Path:** `/games/:gameId/payload`
- **Base URL:** `https://api.scoreboardbuzz.com/api/v1`
- **Official documentation:** [Get Game Payload](https://docs.scoreboardbuzz.com/#/Games/getGamePayload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gameId` | path | `string` | yes | Game ID or managed game ID. |
| `date` | query | `date` | no | Historical date to view in YYYY-MM-DD format. |
