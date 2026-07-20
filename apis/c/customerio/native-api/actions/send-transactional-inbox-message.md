# Send Transactional Inbox Message with Customer.io

Sends a transactional inbox message from Customer.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send/inbox_message`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Send Transactional Inbox Message](https://docs.customer.io/integrations/api/app/#tag/Send%20Messages/operation/sendInboxMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactional_message_id` | body | `string` | yes | The transactional message template to use. You can supply the numeric template ID or the trigger name. |
| `identifiers` | body | `object` | yes | Identifies the person represented by your transactional message by exactly one of id, email, or cio_id. |
| `identifiers.id` | body | `string` | no | Use the customer's ID identifier when your workspace identifies people by ID. |
| `identifiers.email` | body | `string` | no | Use the customer's email identifier when your workspace identifies people by email. |
| `identifiers.cio_id` | body | `string` | no | Use the immutable Customer.io person identifier. |
| `message_data` | body | `object` | no | Key-value pairs referenced by liquid in your inbox message. |
| `to` | body | `string` | no | Optional override for the recipient. |
| `language` | body | `string` | no | Overrides language preferences for the recipient. |
| `send_at` | body | `number` | no | Unix timestamp determining when the message will be sent. |
| `send_to_unsubscribed` | body | `boolean` | no | If false, the message is not sent to unsubscribed recipients. |
| `disable_message_retention` | body | `boolean` | no | If true, the message body is not retained in delivery history. |
| `queue_draft` | body | `boolean` | no | If true, the message is queued as a draft instead of sent immediately. |
