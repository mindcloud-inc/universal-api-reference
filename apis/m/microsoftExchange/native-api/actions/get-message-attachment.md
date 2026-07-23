# Get Message Attachment with Microsoft Exchange

Retrieves a message attachment from Microsoft Exchange.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/messages/{{messageId}}/attachments/{{attachmentId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Message Attachment](https://learn.microsoft.com/en-us/graph/api/attachment-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The Exchange message ID that contains the attachment. |
| `attachmentId` | path | `string` | yes | The Exchange attachment ID returned by the attachment list action. |
