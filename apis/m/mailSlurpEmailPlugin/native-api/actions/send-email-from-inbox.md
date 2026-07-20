# Send Email From Inbox with MailSlurp Email Plugin

Sends an email from an inbox in MailSlurp.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inboxId`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Send Email From Inbox](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxId` | path | `string` | no | The MailSlurp inbox ID to send from. |
