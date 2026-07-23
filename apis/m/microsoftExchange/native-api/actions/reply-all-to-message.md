# Reply All to Message with Microsoft Exchange

Replies to all recipients of a message in Microsoft Exchange.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/replyAll`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Reply All to Message](https://learn.microsoft.com/en-us/graph/api/message-replyall?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Exchange message to reply-all to. |
| `comment` | body | `string` | no | Optional text to include in the reply-all. |
