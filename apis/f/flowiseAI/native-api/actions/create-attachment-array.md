# Create Attachment Array with FlowiseAI

Creates an attachment array for a FlowiseAI chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/attachments/{chatflowId}/{chatId}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Create Attachment Array](https://docs.flowiseai.com/api-reference/attachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatflowId` | path | `string` | yes | Chatflow ID that receives uploaded attachments. |
| `chatId` | path | `string` | yes | Chat session ID for the attachments. |
| `files[]` | body | `array<file>` | yes | Files to upload as multipart form data. Send multiple values as a array. |
