# Send Mail with Microsoft 365 Outlook

Sends a new message from Microsoft 365 Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/sendMail`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Send Mail](https://learn.microsoft.com/en-us/graph/api/user-sendmail?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message.subject` | body | `string` | yes | Email subject. |
| `message.body.content` | body | `string` | yes | Email body content. |
| `message.body.contentType` | body | `list` | yes | Email body content type: Text or HTML. Accepted values: `0`, `1`. |
| `message.toRecipients` | body | `string` | yes | Comma-separated email addresses to send to. Example: person@example.com, other@example.com |
| `saveToSentItems` | body | `boolean` | no | Whether Microsoft should save the sent message to Sent Items. Defaults to true. |
