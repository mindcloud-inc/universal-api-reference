# Get chat messages with Digital Samba

Retrieves room chat messages from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:room/chat`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get chat messages](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms--room--chat)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | path | `string` | yes | Room path parameter. |
| `session_id` | query | `string` | no | UUID of the session. |
| `after` | query | `string` | no | The UUID of the chat message after which records will be returned. |
