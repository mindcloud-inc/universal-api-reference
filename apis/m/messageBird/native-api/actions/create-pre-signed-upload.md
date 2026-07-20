# Create Pre-Signed Upload with MessageBird

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/conversations/:conversationId/presigned-upload`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Create Pre-Signed Upload](https://docs.bird.com/api/conversations-api/api-reference/conversations-messaging/create-pre-signed-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the conversation. |
| `conversationId` | path | `string` | yes | The Bird conversation ID for the upload. |
