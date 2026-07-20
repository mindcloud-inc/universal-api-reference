# Send Test Email with MailSlurp Email Plugin

Sends a test email to an inbox in MailSlurp.

## Endpoint

- **Method:** `POST`
- **Path:** `/inboxes/:inboxId/send-test-email`
- **Base URL:** `https://api.mailslurp.com`
- **Official documentation:** [Send Test Email](https://api.mailslurp.com/swagger-ui/index.html#/InboxController/sendTestEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inboxId` | path | `string` | no | The MailSlurp inbox ID to test. |
