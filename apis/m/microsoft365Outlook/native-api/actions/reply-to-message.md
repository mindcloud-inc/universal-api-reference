# Reply to Message with Microsoft 365 Outlook

Replies to a message in Microsoft 365 Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/reply`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Reply to Message](https://learn.microsoft.com/en-us/graph/api/message-reply?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to reply to. |
| `comment` | body | `string` | no | Optional text to include in the reply. |
