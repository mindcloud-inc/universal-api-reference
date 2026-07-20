# Send Email With Queue with MailSlurp Email Plugin

Sends an email from MailSlurp using the sending queue.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inboxId/with-queue`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Send Email With Queue](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendEmailWithQueue)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxId` | path | `string` | no | The MailSlurp inbox ID to send from. |
