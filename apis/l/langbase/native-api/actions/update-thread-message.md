# Update Thread Message with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/threads/:threadId/messages/:messageId`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Update Thread Message](https://langbase.com/docs/api-reference/threads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadId` | path | `string` | yes | Thread ID that owns the message. |
| `messageId` | path | `string` | yes | Message ID to update. |
| `content` | body | `string` | no | Updated message content. |
