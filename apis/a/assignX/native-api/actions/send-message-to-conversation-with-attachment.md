# Send Message to Conversation with Attachment with AssignX

Sends a message with an attachment in AssignX.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/attachment`
- **Base URL:** `https://api.agentx.so/api/v1/access/`
- **Official documentation:** [Send Message to Conversation with Attachment](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-attachment-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation identifier. |
| `message` | body | `string` | no | Optional message text to send with the attachment. |
| `file` | body | `file` | yes | Attachment file to upload to the conversation. |
