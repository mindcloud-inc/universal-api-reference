# Update Draft Message with Microsoft 365 Outlook

Updates an existing draft message in Microsoft 365 Outlook.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/messages/{{messageId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Update Draft Message](https://learn.microsoft.com/en-us/graph/api/message-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to update. |
| `subject` | body | `string` | no | Updated message subject. This is most useful when editing a draft message. |
| `body.content` | body | `string` | no | Updated message body content. This is most useful when editing a draft message. |
| `body.contentType` | body | `list` | no | The format of the updated body. Only set this when you are also changing the body content — leaving it unset preserves the draft's existing format. Set to HTML when the new body content includes HTML markup, otherwise it is sent as literal text (so HTML tags would show up as visible text). Accepted values: `HTML`, `Text`. |
| `toRecipients` | body | `string` | no | Comma-separated email addresses to set as the draft's recipients, replacing any existing To recipients. This is most useful when editing a draft message. |
| `ccRecipients` | body | `string` | no | Comma-separated email addresses to set as the draft's CC recipients, replacing any existing CC recipients. This is most useful when editing a draft message. |
