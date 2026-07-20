# Show Channel with Stream

Shows a hidden channel in Stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:type/:id/show`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Show Channel](https://getstream.io/chat/docs/javascript/hiding_channels/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Channel type. |
| `id` | path | `string` | yes | Channel ID. |
| `user_id` | body | `string` | yes | User ID performing the show operation. |
