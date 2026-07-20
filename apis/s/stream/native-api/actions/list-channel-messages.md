# List Channel Messages with Stream

Retrieves messages from a specific channel in Stream.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/:type/:id/messages`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [List Channel Messages](https://getstream.io/chat/docs/javascript/channel_pagination/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Channel type. |
| `id` | path | `string` | yes | Channel ID. |
| `ids` | query | `string<string>` | yes | List of message IDs to fetch. |
