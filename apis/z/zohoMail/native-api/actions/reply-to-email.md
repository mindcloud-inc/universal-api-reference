# Reply To Email with Zoho Mail

Replies to an email in Zoho Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/messages/:messageId`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Reply To Email](https://www.zoho.com/mail/help/api/post-reply-to-an-email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID to send the reply from. |
| `messageId` | path | `string` | yes | Message ID of the email you want to reply to. |
| `fromAddress` | body | `string` | yes | Sender email address associated with the authenticated Zoho Mail account. |
| `toAddress` | body | `string` | yes | Recipient email address for the reply. |
| `content` | body | `string` | no | Reply body content. This field is shown in the official sample request. |
| `subject` | body | `string` | no | Reply subject line. |
| `ccAddress` | body | `string` | no | Optional CC recipient email address. |
| `bccAddress` | body | `string` | no | Optional BCC recipient email address. |
| `mailFormat` | body | `list<string>` | no | Format used to send the reply body. Accepted values: `html`, `plaintext`. |
| `askReceipt` | body | `list<string>` | no | Whether to request a read receipt from the recipient. Accepted values: `no`, `yes`. |
| `encoding` | body | `list<string>` | no | Character encoding for the reply content. Accepted values: `Big5`, `EUC-JP`, `EUC-KR`, `GB2312`, `ISO-2022-JP`, `ISO-8859-1`, `KOI8-R`, `Shift_JIS`, `US-ASCII`, `UTF-8`, `WINDOWS-1251`, `X-WINDOWS-ISO2022JP`. |
| `isSchedule` | body | `boolean` | no | Whether to schedule the reply instead of sending it immediately. |
| `scheduleType` | body | `list<number>` | no | Scheduling preset to use when sending the reply later. Accepted values: `1`, `2`, `3`, `4`, `5`, `6`. |
| `timeZone` | body | `string` | no | Time zone used for a custom scheduled reply when Schedule Type is 6. |
| `scheduleTime` | body | `string` | no | Custom date and time for the scheduled reply in MM/DD/YYYY HH:MM:SS format. |
