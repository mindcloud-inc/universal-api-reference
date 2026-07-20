# Send chat message with Digital Samba

Creates a room chat message in Digital Samba.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:room/chat`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Send chat message](https://developer.digitalsamba.com/rest-api/#rooms-POSTapi-v1-rooms--room--chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | path | `string` | yes | Room path parameter. |
| `body` | body | `object` | no | JSON request body documented for this endpoint. |
| `message` | body | `string` | no | Chat message. |
