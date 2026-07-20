# List Message Attachments with Outlook

Retrieves attachments for an Outlook email.

## Endpoint

- **Method:** `GET`
- **Path:** `/me/messages/:messageId/attachments`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [List Message Attachments](https://learn.microsoft.com/en-us/graph/api/message-list-attachments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Microsoft Graph ID of the Outlook message whose attachments should be listed. |
