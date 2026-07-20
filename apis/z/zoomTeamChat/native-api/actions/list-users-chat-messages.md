# List User's Chat Messages with Zoom Team Chat

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/users/:userId/messages`
- **Base URL:** `https://api.zoom.us/v2`
- **Official documentation:** [List User's Chat Messages](https://developers.zoom.us/docs/api/rest/reference/chat/methods/#operation/getChatMessages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The unique identifier of the user. |
| `to_contact` | query | `string` | no | Query messages for a specific contact. |
| `to_channel` | query | `string` | no | Query messages for a specific channel. |
| `date` | query | `string` | no | Query date in YYYY-MM-DD format. |
| `from` | query | `string` | no | Start timestamp in ISO-8601 format. |
| `to` | query | `string` | no | End timestamp in ISO-8601 format. |
| `search_type` | query | `string` | no | Search scope such as message or file. |
| `search_key` | query | `string` | no | Search text for message or file content. |
