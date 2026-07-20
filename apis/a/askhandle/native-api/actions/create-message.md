# Create Message with AskHandle

Creates a new message in an AskHandle room.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/`
- **Base URL:** `https://dashboard.askhandle.com/api/v1`
- **Official documentation:** [Create Message](https://dashboard.askhandle.com/api/v1/docs/api_reference.html#message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Message body. |
| `email` | body | `string` | no | Message sender email. |
| `nickname` | body | `string` | no | Message sender nickname. |
| `room.uuid` | body | `string` | no | The UUID of the room that will receive the message. |
