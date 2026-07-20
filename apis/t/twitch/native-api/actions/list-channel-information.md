# List Channel Information with Twitch

Retrieves broadcaster channel information from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Channel Information](https://dev.twitch.tv/docs/api/reference#get-channel-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster whose channel you want to get. |
