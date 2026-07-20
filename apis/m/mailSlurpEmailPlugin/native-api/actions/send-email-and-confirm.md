# Send Email And Confirm with MailSlurp Email Plugin

Sends an email from MailSlurp and returns the confirmation.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inboxId/confirm`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Send Email And Confirm](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendEmailAndConfirm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxId` | path | `string` | no | The MailSlurp inbox ID to send from. |
