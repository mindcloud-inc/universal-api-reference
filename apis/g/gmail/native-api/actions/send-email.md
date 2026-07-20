# Send Email with Google Mail

Sends a Gmail message.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/send`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Send Email](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient email address. Use a comma-separated list for multiple recipients. |
| `subject` | body | `string` | yes | Email subject line. |
| `bodyText` | body | `string` | no | Plain-text email body, if both Body Text and Body Email are used, Body Text will be rendered above Body HTML. |
| `bodyHtml` | body | `string` | no | HTML email body, if both Body Text and Body Email are used, Body Text will be rendered above Body HTML. |
| `attachmentFile` | body | `file` | no | Optional single attachment file to include with the email. |
| `cc` | body | `string` | no | Optional CC recipients. Use a comma-separated list. |
| `bcc` | body | `string` | no | Optional BCC recipients. Use a comma-separated list. |
| `from` | body | `string` | no | Optional sender header. Must be permitted by Gmail account configuration. |
| `replyTo` | body | `string` | no | Optional Reply-To address. |
| `threadId` | body | `string` | no | Optional Gmail thread ID to reply in an existing thread. |
| `attachmentFilename` | body | `string` | no | Optional attachment filename override. Defaults to the uploaded file name when available. |
| `attachmentMimeType` | body | `string` | no | Optional attachment MIME type override. Defaults to application/octet-stream when unknown. |
