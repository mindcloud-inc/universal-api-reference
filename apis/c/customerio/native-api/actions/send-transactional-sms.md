# Send Transactional SMS with Customer.io

Sends a transactional SMS from Customer.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send/sms`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Send Transactional SMS](https://docs.customer.io/integrations/api/app/#tag/Send%20Messages/operation/sendSMS)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactional_message_id` | body | `string` | yes | The transactional message template to use. You can supply the numeric template ID or the trigger name. |
| `to` | body | `string` | yes | The phone number to send the SMS to in E.164 format, or a liquid reference. |
| `identifiers` | body | `object` | yes | Identifies the person represented by your transactional message by exactly one of id, email, or cio_id. |
| `identifiers.id` | body | `string` | no | Use the customer's ID identifier when your workspace identifies people by ID. |
| `identifiers.email` | body | `string` | no | Use the customer's email identifier when your workspace identifies people by email. |
| `identifiers.cio_id` | body | `string` | no | Use the immutable Customer.io person identifier. |
| `from` | body | `string` | no | The verified phone number or sender ID that the SMS is from. |
| `language` | body | `string` | no | Overrides language preferences for the recipient. |
| `message_data` | body | `object` | no | Key-value pairs referenced by liquid in your message. |
| `send_at` | body | `number` | no | Unix timestamp determining when the message will be sent. |
| `send_to_unsubscribed` | body | `boolean` | no | If false, the message is not sent to unsubscribed recipients. |
| `disable_message_retention` | body | `boolean` | no | If true, the message body is not retained in delivery history. |
| `queue_draft` | body | `boolean` | no | If true, the message is queued as a draft instead of sent immediately. |
