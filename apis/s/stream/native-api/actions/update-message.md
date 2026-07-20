# Update Message with Stream

Updates an existing message in Stream.

## Endpoint

- **Method:** `PUT`
- **Path:** `/messages/:id`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Update Message](https://getstream.io/chat/docs/javascript/send_message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Message ID. |
| `set` | body | `object` | no | Fields to set on the message. |
| `user_id` | body | `string` | yes | User ID performing the message update. |
