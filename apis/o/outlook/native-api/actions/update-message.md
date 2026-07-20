# Update Message with Outlook

Updates an existing Outlook email, with some fields draft-only.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/me/messages/:messageId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Update Message](https://learn.microsoft.com/en-us/graph/api/message-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | Microsoft Graph ID of the message to update. |
| `subject` | body | `string` | no | New message subject. Updatable only for drafts. |
| `body.content` | body | `string` | no | New message body content. Updatable only for drafts. |
| `body.contentType` | body | `list` | no | Message body content type: Text or HTML. Accepted values: `0`, `1`. |
| `isRead` | body | `boolean` | no | Whether the message should be marked as read. |
| `categories[]` | body | `array<string>` | no | Categories to apply to the message. |
| `importance` | body | `list` | no | Message importance: low, normal, or high. Accepted values: `0`, `1`, `2`. |
| `inferenceClassification` | body | `list` | no | Focused inbox classification: focused or other. Accepted values: `0`, `1`. |
