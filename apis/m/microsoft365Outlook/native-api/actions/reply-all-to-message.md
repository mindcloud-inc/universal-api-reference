# Reply All to Message with Microsoft 365 Outlook

Replies to all recipients of a message in Microsoft 365 Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/replyAll`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Reply All to Message](https://learn.microsoft.com/en-us/graph/api/message-replyall?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to reply-all to. |
| `comment` | body | `string` | no | Optional text to include in the reply-all. |
| `message.toRecipients` | body | `string` | no | Optional. Comma-separated email addresses to override who the reply-all is sent to, instead of the original message's sender/replyTo/recipients. Example: person@example.com, other@example.com |
| `message.ccRecipients` | body | `string` | no | Optional. Comma-separated email addresses to CC on the reply-all. Example: person@example.com, other@example.com |
