# List Channel Emotes with Twitch

Retrieves channel emote records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/emotes`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Channel Emotes](https://dev.twitch.tv/docs/api/reference#get-channel-emotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | An ID that identifies the broadcaster whose emotes you want to get. |
