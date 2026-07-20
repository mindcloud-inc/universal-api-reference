# List Message Attachments with Microsoft 365

Retrieves message attachments from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/messages/{{messageId}}/attachments`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Message Attachments](https://learn.microsoft.com/en-us/graph/api/message-list-attachments?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The Outlook message ID whose attachments you want to list. |
