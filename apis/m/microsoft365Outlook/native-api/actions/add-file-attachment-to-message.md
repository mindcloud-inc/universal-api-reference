# Add File Attachment to Message with Microsoft 365 Outlook

Adds a file attachment to a message in Microsoft 365 Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/attachments`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Add File Attachment to Message](https://learn.microsoft.com/en-us/graph/api/message-post-attachments?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The draft or message ID to attach the file to. |
| `name` | body | `string` | yes | Name of the file attachment. |
| `contentType` | body | `string` | yes | MIME type of the attachment content. |
| `contentBytes` | body | `string` | yes | Base64-encoded file content. Microsoft Graph supports this action for attachments under 3 MB. |
