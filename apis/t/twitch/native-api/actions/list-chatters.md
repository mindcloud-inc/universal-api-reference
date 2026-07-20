# List Chatters with Twitch

Retrieves channel chatter records from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/chatters`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Chatters](https://dev.twitch.tv/docs/api/reference#get-chatters)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | ID of the broadcaster whose chatters you want to list. |
| `moderator_id` | query | `string` | yes | ID of the moderator or broadcaster making the request. Must match the user in the OAuth token. |
| `first` | query | `number` | no | Maximum number of chatters to return. Minimum 1, maximum 1,000. |
| `after` | query | `string` | no | Cursor for forward pagination. |
