# Send Message With Attachment with AgentX

Sends a message with an attachment in AgentX.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:id/attachment`
- **Base URL:** `https://api.agentx.so/api/v1/access`
- **Official documentation:** [Send Message With Attachment](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-attachment-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation Id |
| `file` | body | `file` | no | File to upload |
| `message` | body | `string` | no | Message to send |
| `context` | body | `number` | no | Context for the message |
