# Archive Emails with Zoho Mail

Archives email messages in Zoho Mail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/updatemessage`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Archive Emails](https://www.zoho.com/mail/help/api/put-archive-email.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `messageId[]` | body | `array<string>` | no | One or more message IDs to archive. |
| `threadId[]` | body | `array<string>` | no | One or more thread IDs to archive instead of specific message IDs. |
