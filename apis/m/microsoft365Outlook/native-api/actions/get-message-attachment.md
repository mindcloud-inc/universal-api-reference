# Get Message Attachment with Microsoft 365 Outlook

Retrieves an attachment from Microsoft 365 Outlook.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/messages/{{messageId}}/attachments/{{attachmentId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Message Attachment](https://learn.microsoft.com/en-us/graph/api/attachment-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The Outlook message ID that contains the attachment. |
| `attachmentId` | path | `string` | yes | The Outlook attachment ID returned by the attachment list action. |
