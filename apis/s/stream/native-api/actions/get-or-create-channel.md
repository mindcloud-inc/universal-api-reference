# Get Or Create Channel with Stream

Finds a channel in Stream, or creates it if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels/:type/:id/query`
- **Base URL:** `https://chat.stream-io-api.com`
- **Official documentation:** [Get Or Create Channel](https://getstream.io/chat/docs/javascript/channel_pagination/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Channel type. |
| `id` | path | `string` | yes | Channel ID. |
| `data` | body | `object` | no | Channel creation/update payload. |
| `state` | body | `boolean` | no | Whether to return channel state. |
