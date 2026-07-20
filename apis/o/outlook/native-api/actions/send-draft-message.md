# Send Draft Message with Outlook

Sends an existing draft email from Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/me/messages/:messageId/send`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Send Draft Message](https://learn.microsoft.com/en-us/graph/api/message-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Microsoft Graph ID of the draft message to send. |
