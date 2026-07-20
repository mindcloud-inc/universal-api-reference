# Find Chat Versions with v0

Finds versions for a v0 chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/:chatId/versions`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Find Chat Versions](https://v0.app/docs/api/platform/reference/chats/find-versions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat whose versions to list. |
| `limit` | query | `number` | no | Specifies the maximum number of version records to return in a single response. |
| `cursor` | query | `string` | no | Base64 encoded cursor containing pagination data. |
