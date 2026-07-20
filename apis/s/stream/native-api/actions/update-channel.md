# Update Channel with Stream

Updates an existing channel in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:type/:id`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Update Channel](https://getstream.io/chat/docs/javascript/channel_update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Channel type. |
| `id` | path | `string` | yes | Channel ID. |
| `data` | body | `object` | no | Channel update payload. |
| `message` | body | `object` | no | Optional system message to send with the update. |
