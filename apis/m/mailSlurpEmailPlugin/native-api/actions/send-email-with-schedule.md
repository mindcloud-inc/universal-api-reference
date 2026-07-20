# Send Email With Schedule with MailSlurp Email Plugin

Schedules an email to send from MailSlurp.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inboxId/with-schedule`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Send Email With Schedule](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendWithSchedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxId` | path | `string` | no | The MailSlurp inbox ID to send from. |
