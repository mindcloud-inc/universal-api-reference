# Get Chat Settings with Twitch

Retrieves channel chat settings from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/settings`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Get Chat Settings](https://dev.twitch.tv/docs/api/reference#get-chat-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster whose chat settings you want to get. |
| `moderator_id` | query | `string` | no | The ID of a moderator in the broadcaster’s channel. Include this only when you need the non-moderator chat delay fields. |
