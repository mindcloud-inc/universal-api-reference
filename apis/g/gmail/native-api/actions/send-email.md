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
| `bodyText` | body | `string` | no | Plain-text alternative to Body HTML. Email clients select the supported representation when both are provided. |
| `bodyHtml` | body | `string` | no | HTML email body. Map htmlContent from Get Email to retain the original markup. |
| `attachmentFile` | body | `file` | no | Optional single attachment file to include with the email. |
| `cc` | body | `string` | no | Optional CC recipients. Use a comma-separated list. |
| `bcc` | body | `string` | no | Optional BCC recipients. Use a comma-separated list. |
| `from` | body | `string` | no | Optional sender header. Must be permitted by Gmail account configuration. |
| `replyTo` | body | `string` | no | Optional Reply-To address. |
| `threadId` | body | `string` | no | Optional Gmail thread ID to reply in an existing thread. |
| `attachments[]` | body | `array<object>` | no | Add one item per attachment. Each item contains Filename, MIME Type, and Base64 Data. For Gmail attachments, use the data returned by Get Email Attachment. |
| `attachments[].filename` | body | `string` | yes | — |
| `attachments[].mimeType` | body | `string` | no | Defaults to application/octet-stream. |
| `attachments[].data` | body | `string` | yes | File content encoded as base64 or base64url. Accepts the data returned by Get Email Attachment; do not supply a URL or an attachment ID. |
| `attachmentFilename` | body | `string` | no | Optional attachment filename override. Defaults to the uploaded file name when available. |
| `attachmentMimeType` | body | `string` | no | Optional attachment MIME type override. Defaults to application/octet-stream when unknown. |
