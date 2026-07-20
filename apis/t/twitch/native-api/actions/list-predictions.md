# List Predictions with Twitch

Retrieves broadcaster prediction records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/predictions`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Predictions](https://dev.twitch.tv/docs/api/reference#get-predictions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | ID of the broadcaster whose predictions you want to read. Must match the user in the OAuth token. |
| `id` | query | `string` | no | Optional prediction ID filter. Twitch accepts up to 25 IDs. Send multiple values as a array. |
