# Delete Message with Stream

Deletes an existing message from Stream.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/messages/:id`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Delete Message](https://getstream.io/chat/docs/javascript/send_message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Message ID. |
| `hard` | query | `boolean` | no | Whether to hard delete the message. |
