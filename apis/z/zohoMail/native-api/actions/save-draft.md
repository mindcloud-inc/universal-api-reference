# Save Draft with Zoho Mail

Creates a draft email in Zoho Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/messages`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Save Draft](https://www.zoho.com/mail/help/api/post-save-draft-template.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `fromAddress` | body | `string` | yes | Sender email address. |
| `toAddress` | body | `string` | no | Comma-separated recipient email addresses. |
| `subject` | body | `string` | no | Draft subject line. |
| `content` | body | `string` | no | Draft body content. |
| `ccAddress` | body | `string` | no | Comma-separated CC recipient email addresses. |
| `bccAddress` | body | `string` | no | Comma-separated BCC recipient email addresses. |
| `mailFormat` | body | `list<string>` | no | Body format. Accepted values: `html`, `plaintext`. |
| `askReceipt` | body | `list<string>` | no | Whether to request a read receipt when the draft is sent. Accepted values: `no`, `yes`. |
| `encoding` | body | `string` | no | Body content encoding. |
| `inReplyTo` | body | `string` | no | Original message reference for threading. |
| `refHeader` | body | `string` | no | Reference headers for threading. |
