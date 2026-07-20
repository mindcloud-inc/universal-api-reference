# List Channel Editors with Twitch

Retrieves channel editor records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/editors`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Channel Editors](https://dev.twitch.tv/docs/api/reference#get-channel-editors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster that owns the channel. |
