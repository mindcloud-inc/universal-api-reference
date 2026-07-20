# List Message Attachments with Microsoft 365 Outlook

Retrieves attachments for a message from Microsoft 365 Outlook.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/messages/{{messageId}}/attachments`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Message Attachments](https://learn.microsoft.com/en-us/graph/api/message-list-attachments?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The Outlook message ID whose attachments you want to list. |
