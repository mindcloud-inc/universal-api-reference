# Hide Channel with Stream

Hides a channel in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:type/:id/hide`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Hide Channel](https://getstream.io/chat/docs/javascript/hiding_channels/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Channel type. |
| `id` | path | `string` | yes | Channel ID. |
| `clear_history` | body | `boolean` | no | Whether to clear message history when hiding the channel. |
| `user_id` | body | `string` | yes | User ID performing the hide operation. |
