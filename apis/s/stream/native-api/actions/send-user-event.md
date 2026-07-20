# Send User Event with Stream

Sends a custom event to a user in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user_id/event`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Send User Event](https://getstream.io/chat/docs/javascript/event_object/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `string` | yes | User ID to send the event to. |
| `event` | body | `object` | yes | Custom event payload. |
