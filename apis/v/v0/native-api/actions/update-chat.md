# Update Chat with v0

Updates an existing chat in v0.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/chats/:chatId`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Update Chat](https://v0.app/docs/api/platform/reference/chats/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat to update. |
| `name` | body | `string` | no | — |
| `privacy` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
