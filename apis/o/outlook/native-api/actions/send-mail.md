# Send Mail with Outlook

Sends a new email from Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/me/sendMail`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Send Mail](https://learn.microsoft.com/en-us/graph/api/user-sendmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message.subject` | body | `string` | yes | Email subject. |
| `message.body.content` | body | `string` | yes | Email body content. |
| `message.body.contentType` | body | `list` | yes | Email body content type: Text or HTML. Accepted values: `0`, `1`. |
| `message.toRecipients` | body | `string<object>` | yes | Comma-separated email addresses to send to. Example: person@example.com, other@example.com |
| `saveToSentItems` | body | `boolean` | no | Whether Microsoft should save the sent message to Sent Items. Defaults to true. |
