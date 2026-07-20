# Send Email with lemlist

Sends an email from lemlist inbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/email`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Send Email](https://developer.lemlist.com/api-reference/endpoints/inbox/send-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sendUserId` | body | `string` | yes | Sender user ID. |
| `sendUserEmail` | body | `string` | yes | Sender email address. |
| `sendUserMailboxId` | body | `string` | yes | Sender mailbox ID. |
| `contactId` | body | `string` | yes | Contact ID. |
| `leadId` | body | `string` | yes | Lead ID. |
| `subject` | body | `string` | yes | Email subject. |
| `message` | body | `string` | yes | Email message (HTML). |
| `cc[]` | body | `array<string>` | no | CC email addresses. |
