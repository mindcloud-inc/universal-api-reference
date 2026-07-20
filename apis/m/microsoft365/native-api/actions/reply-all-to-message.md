# Reply All to Message with Microsoft 365

Replies to all recipients on a message in Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/replyAll`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Reply All to Message](https://learn.microsoft.com/en-us/graph/api/message-replyall?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to reply-all to. |
| `comment` | body | `string` | no | Optional text to include in the reply-all. |
