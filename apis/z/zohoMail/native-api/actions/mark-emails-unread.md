# Mark Emails Unread with Zoho Mail

Marks emails as unread in Zoho Mail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/updatemessage`
- **Base URL:** `https://mail.zoho.com/api`
- **Official documentation:** [Mark Emails Unread](https://www.zoho.com/mail/help/api/put-mark-email-as-unread.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `list<string>` | yes | Zoho Mail account ID. |
| `messageId[]` | body | `array<string>` | no | One or more message IDs to mark as unread. |
| `threadId[]` | body | `array<string>` | no | One or more thread IDs to mark as unread instead of specific message IDs. |
