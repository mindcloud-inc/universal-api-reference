# Get Email Attachment with Google Mail

Retrieves a Gmail message attachment.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/:messageId/attachments/:id`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Get Email Attachment](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages.attachments/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The Gmail message ID that contains the attachment. |
| `id` | path | `string` | yes | Attachment ID from the message payload. |
