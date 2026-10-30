# Create Draft Message with Microsoft 365 Outlook

Creates a draft message in Microsoft 365 Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Draft Message](https://learn.microsoft.com/en-us/graph/api/user-post-messages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `toRecipients` | body | `string` | no | Comma-separated email addresses to add as draft recipients. Example: person@example.com, other@example.com |
| `ccRecipients` | body | `string` | no | Comma-separated email addresses to CC on the draft. Example: person@example.com, other@example.com |
| `subject` | body | `string` | no | The draft email subject line. |
| `body.content` | body | `string` | no | The draft email body content. |
| `body.contentType` | body | `list` | no | The format of the draft body. Set to HTML when the body content includes HTML markup, otherwise it is sent as literal text (so HTML tags would show up as visible text). Accepted values: `HTML`, `Text`. |
