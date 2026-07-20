# List Polls with Twitch

Retrieves broadcaster poll records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/polls`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Polls](https://dev.twitch.tv/docs/api/reference#get-polls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | ID of the broadcaster whose polls you want to read. Must match the user in the OAuth token. |
| `id` | query | `string` | no | Optional poll ID filter. Twitch accepts up to 20 IDs. Send multiple values as a array. |
