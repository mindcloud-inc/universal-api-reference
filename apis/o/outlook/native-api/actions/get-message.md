# Get Message with Outlook

Retrieves an email from Outlook by message ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/me/messages/:messageId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Get Message](https://learn.microsoft.com/en-us/graph/api/message-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Microsoft Graph ID of the Outlook message to retrieve. |
