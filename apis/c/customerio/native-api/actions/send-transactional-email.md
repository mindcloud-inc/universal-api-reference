# Send Transactional Email with Customer.io

Sends a transactional email from Customer.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send/email`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Send Transactional Email](https://docs.customer.io/integrations/api/app/#tag/Send%20Messages/operation/sendEmail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactional_message_id` | body | `string` | yes | The transactional message template to use. You can supply the numeric template ID or the trigger name. |
| `identifiers` | body | `object` | yes | Identifies the person represented by your transactional message by exactly one of id, email, or cio_id. |
| `identifiers.id` | body | `string` | no | Use the customer's ID identifier when your workspace identifies people by ID. |
| `identifiers.email` | body | `string` | no | Use the customer's email identifier when your workspace identifies people by email. |
| `identifiers.cio_id` | body | `string` | no | Use the immutable Customer.io person identifier. |
| `to` | body | `string` | yes | The message recipient or recipients. |
| `from` | body | `string` | no | The verified sender address that the email is from. |
| `subject` | body | `string` | no | Overrides the transactional template subject line. |
| `body` | body | `string` | no | Overrides the transactional template HTML body. |
| `body_plain` | body | `string` | no | Overrides the plaintext body. |
| `message_data` | body | `object` | no | Key-value pairs referenced by liquid in your message. |
| `language` | body | `string` | no | Overrides language preferences for the recipient. |
| `send_at` | body | `number` | no | Unix timestamp determining when the message will be sent. |
| `send_to_unsubscribed` | body | `boolean` | no | If false, the message is not sent to unsubscribed recipients. |
| `disable_message_retention` | body | `boolean` | no | If true, the message body is not retained in delivery history. |
| `queue_draft` | body | `boolean` | no | If true, the message is queued as a draft instead of sent immediately. |
| `body_amp` | body | `string` | no | AMP-enabled email body. |
| `bcc` | body | `string` | no | Blind copy recipients. |
| `fake_bcc` | body | `boolean` | no | If true, Customer.io sends per-recipient copies instead of true BCC copies. |
| `reply_to` | body | `string` | no | The address that recipients can reply to. |
| `preheader` | body | `string` | no | Preview text shown next to or under the subject line. |
| `attachments` | body | `object` | no | A dictionary of attachments keyed by filename with base64-encoded contents. |
| `headers` | body | `string` | no | A JSON string containing an array of header objects. |
| `disable_css_preprocessing` | body | `boolean` | no | If true, disables CSS preprocessing for the email. |
| `tracked` | body | `boolean` | no | If true, Customer.io tracks opens and link clicks in your message. |
