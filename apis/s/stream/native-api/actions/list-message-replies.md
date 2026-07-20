# List Message Replies with Stream

Retrieves replies from a message thread in Stream.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:parent_id/replies`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [List Message Replies](https://getstream.io/chat/docs/javascript/threads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent_id` | path | `string` | yes | Parent message ID. |
| `limit` | query | `number` | no | Maximum number of replies to return. |
