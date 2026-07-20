# Mark Emails Read with Zoho Mail

Marks emails as read in Zoho Mail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/updatemessage`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Mark Emails Read](https://www.zoho.com/mail/help/api/put-mark-email-as-read.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `messageId[]` | body | `array<string>` | no | One or more message IDs to mark as read. |
| `threadId[]` | body | `array<string>` | no | One or more thread IDs to mark as read instead of specific message IDs. |
