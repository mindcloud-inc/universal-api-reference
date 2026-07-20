# Send Message with Stream

Creates a new message in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:type/:id/message`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Send Message](https://getstream.io/chat/docs/javascript/send_message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Channel type. |
| `id` | path | `string` | yes | Channel ID. |
| `message` | body | `object` | yes | Message payload. |
