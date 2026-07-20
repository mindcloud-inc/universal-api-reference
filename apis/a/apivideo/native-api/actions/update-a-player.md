# Update a player with api.video

Updates an existing player theme in api.video.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/players/:playerId`
- **Base URL:** `https://ws.api.video`
- **Official documentation:** [Update a player](https://docs.api.video/reference/api/Player-Themes#update-a-player)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional updated display name for the player theme. |
| `playerId` | path | `string` | yes | The unique identifier for the player theme. |
