# Get Chat Version with v0

Retrieves a chat version from v0 by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/chats/:chatId/versions/:versionId`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Get Chat Version](https://v0.app/docs/api/platform/reference/chats/get-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat that owns the version. |
| `versionId` | path | `string` | yes | The ID of the chat version to retrieve. |
