# Delete Message with Outlook

Deletes an existing email from Outlook.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/me/messages/:messageId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Delete Message](https://learn.microsoft.com/en-us/graph/api/message-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Microsoft Graph ID of the message to delete. |
