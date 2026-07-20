# Send Triggered Email with Wooxy

Sends a triggered email through Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/mailer/trigger`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Send Triggered Email](https://wooxy.com/api-documentation/email/send-triggered-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | yes | The Wooxy contact list ID. The list must already exist in your account. |
| `contact` | body | `string` | yes | The recipient email, user ID, or phone number already stored in the contact list. |
| `templateId` | body | `string` | yes | The Wooxy template ID to send. |
| `ignoreBlackList` | body | `boolean` | no | Whether to ignore black list status for the send. |
