# Send Batch Triggered Email with Wooxy

Sends batch triggered emails through Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/mailer/batch-trigger`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Send Batch Triggered Email](https://wooxy.com/api-documentation/email/send-batch-triggered-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | yes | The Wooxy contact list ID. The list must already exist in your account. |
| `templateId` | body | `string` | yes | The Wooxy template ID to send. |
| `contacts[]` | body | `array<object>` | yes | The contacts array, for example [{"contact":"user@example.com"}]. |
