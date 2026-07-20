# List Games with Twitch

Retrieves game category records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/games`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Games](https://dev.twitch.tv/docs/api/reference#get-games)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | The ID of the game to get. Specify this parameter up to 100 times. Send multiple values as a array. |
| `name` | query | `string` | no | The name of the game to get. Specify this parameter up to 100 times. Send multiple values as a array. |
| `igdb_id` | query | `string` | no | The IGDB ID of the game to get. Specify this parameter up to 100 times. Send multiple values as a array. |
