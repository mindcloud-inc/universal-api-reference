# Send Mail with Microsoft 365

Sends an email from Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/sendMail`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Send Mail](https://learn.microsoft.com/en-us/graph/api/user-sendmail?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message.toRecipients` | body | `string<object>` | yes | Comma-separated email addresses to send to. Example: person@example.com, other@example.com |
| `message.subject` | body | `string` | no | The email subject line. |
| `message.body.content` | body | `string` | no | The text content of the email body. |
| `message.ccRecipients` | body | `string` | no | Optional CC recipients. Use a comma separated list. |
| `message.bccRecipients` | body | `string` | no | Optional BCC recipients. Use a comma separated list. |
| `message.attachments` | body | `file` | no | Optional single attachment file to include with the email. |
| `attachmentFilename` | body | `string` | no | Optional attachment filename override. Defaults to the uploaded file name when available. |
| `attachmentMimeType` | body | `string` | no | Optional attachment MIME type override. Defaults to application/octet-stream when unknown. |
