# Send Email with Zoho Mail

Sends an email through Zoho Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/messages`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Send Email](https://www.zoho.com/mail/help/api/post-send-an-email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `fromAddress` | body | `string` | yes | Sender email address. |
| `toAddress` | body | `string` | yes | Comma-separated recipient email addresses. |
| `subject` | body | `string` | no | Email subject line. |
| `content` | body | `string` | no | Email body content. |
| `ccAddress` | body | `string` | no | Comma-separated CC recipient email addresses. |
| `bccAddress` | body | `string` | no | Comma-separated BCC recipient email addresses. |
| `mailFormat` | body | `list<string>` | no | Body format. Accepted values: `html`, `plaintext`. |
| `askReceipt` | body | `list<string>` | no | Whether to request a read receipt. Accepted values: `no`, `yes`. |
| `encoding` | body | `string` | no | Body content encoding. |
| `isSchedule` | body | `boolean` | no | Whether to schedule the email instead of sending immediately. |
| `scheduleType` | body | `list<string>` | no | Scheduling rule type. Accepted values: `1`, `2`, `3`, `4`, `5`, `6`. |
| `timeZone` | body | `string` | no | Time zone to use when scheduling by specific date and time. |
| `scheduleTime` | body | `string` | no | Scheduled send time in Zoho Mail format. |
